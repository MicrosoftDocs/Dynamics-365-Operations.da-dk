---
title: Lagerlokationer
description: Lagerlokationer bruges sammen med grundlæggende lagersted (WMS I) til at bestemme, hvor varerne opbevares, og hvor varerne plukkes fra i et WMS I-lagersted.
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSLocation
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2134
ms.assetid: 69bf6922-4151-447f-b678-4ba95637f54c
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ce1e33fab6704dd3387f0c2034a8a950a858b2e0
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/18/2019
ms.locfileid: "2814300"
---
# <a name="inventory-locations"></a><span data-ttu-id="6fb4b-103">Lagerlokationer</span><span class="sxs-lookup"><span data-stu-id="6fb4b-103">Inventory locations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6fb4b-104">Lagerlokationer bruges sammen med grundlæggende lagersted (WMS I) til at bestemme, hvor varerne opbevares, og hvor varerne plukkes fra i et WMS I-lagersted.</span><span class="sxs-lookup"><span data-stu-id="6fb4b-104">Inventory locations are used with basic warehousing (WMS I) to determine where items are stored and where items are picked from in a WMS I warehouse.</span></span>

<span data-ttu-id="6fb4b-105">Dette emne gælder for funktioner i modulet Lagerstyring.</span><span class="sxs-lookup"><span data-stu-id="6fb4b-105">This topic applies to features in the Inventory management module.</span></span> <span data-ttu-id="6fb4b-106">Det gælder ikke for funktioner i modulet Lagerstedsstyring.</span><span class="sxs-lookup"><span data-stu-id="6fb4b-106">It does not apply to features in the Warehouse management module.</span></span>

<span data-ttu-id="6fb4b-107">Betegnelsen lokalitet henviser til det sted, som varer opbevares på og trækkes fra.</span><span class="sxs-lookup"><span data-stu-id="6fb4b-107">The term location refers to the place that items are stored and drawn from.</span></span>

<span data-ttu-id="6fb4b-108">For hver lokation kan der også angives det sted, hvor varen indsættes.</span><span class="sxs-lookup"><span data-stu-id="6fb4b-108">For each location, the place where the item is inserted can also be specified.</span></span> <span data-ttu-id="6fb4b-109">Som standard er de ens.</span><span class="sxs-lookup"><span data-stu-id="6fb4b-109">By default, they are the same.</span></span> <span data-ttu-id="6fb4b-110">Varer indsættes og trækkes normalt fra den samme side af en lokation, men ikke altid.</span><span class="sxs-lookup"><span data-stu-id="6fb4b-110">Items are usually inserted and drawn from the same side of a location, but not always.</span></span> <span data-ttu-id="6fb4b-111">Varer, der opbevares i lagerreoler med rullebaner, indsættes fra én gang og trækkes fra en anden.</span><span class="sxs-lookup"><span data-stu-id="6fb4b-111">For example, items that are stored in live storage racks are inserted from one aisle and drawn from another.</span></span> <span data-ttu-id="6fb4b-112">Hovedindlagringsstedet angives i form af et lokationsnavn, der normalt bestemmes ved dets koordinater: lager, gang, reol, hylde og beholder.</span><span class="sxs-lookup"><span data-stu-id="6fb4b-112">The main input is given by a location name, which is usually determined by its coordinates: warehouse, aisle, rack, shelf, and bin.</span></span> <span data-ttu-id="6fb4b-113">Dette navn eller id kan angives manuelt eller genereres på basis af lokationens koordinater – f.eks. 01-02-03-4, som står for gang 1, reol 2, hylde 3, beholder 4 på siden Lagerlokationer.</span><span class="sxs-lookup"><span data-stu-id="6fb4b-113">This name or ID can be entered manually or generated from the location coordinates—for example, 01-02-03-4 for aisle 1, rack 2, shelf 3, bin 4 in the Inventory locations page.</span></span>
<span data-ttu-id="6fb4b-114">Lokationsegenskaber</span><span class="sxs-lookup"><span data-stu-id="6fb4b-114">Location properties</span></span>

<span data-ttu-id="6fb4b-115">Lokationen har følgende koordinater:</span><span class="sxs-lookup"><span data-stu-id="6fb4b-115">A location has the following characteristics:</span></span>
-   <span data-ttu-id="6fb4b-116">Størrelse (højde, bredde, dybde og derved rumfang)</span><span class="sxs-lookup"><span data-stu-id="6fb4b-116">Size (height, width, depth, and thereby volume)</span></span>
-   <span data-ttu-id="6fb4b-117">Lagersted, gang, reol, hylde og beholder</span><span class="sxs-lookup"><span data-stu-id="6fb4b-117">Warehouse, aisle, rack, shelf, and bin position</span></span>
-   <span data-ttu-id="6fb4b-118">Placeringstype (bulkvarelokation, plukplads, modtagelsesområde, forsendelsesområde, produktionsindlagringslokation, inspektionssted eller kanban-supermarked)</span><span class="sxs-lookup"><span data-stu-id="6fb4b-118">Location type (bulk location, picking location, inbound dock, outbound dock, production input location, inspection location, or kanban supermarket)</span></span>

<span data-ttu-id="6fb4b-119">I onlinesystemer kan der anvendes kontroltekst, som sikrer, at operatøren har valgt den rigtige lokation til en bestemt vare.</span><span class="sxs-lookup"><span data-stu-id="6fb4b-119">Check text can be used in online systems to verify that the operator has selected the correct location for a specific item.</span></span> <span data-ttu-id="6fb4b-120">Kontrolteksten kan oprettes manuelt, eller der kan indsættes en standardtekst.</span><span class="sxs-lookup"><span data-stu-id="6fb4b-120">This check text can be created manually or by default.</span></span>

## <a name="sort-codes"></a><span data-ttu-id="6fb4b-121">Sorteringskoder</span><span class="sxs-lookup"><span data-stu-id="6fb4b-121">Sort codes</span></span>
<span data-ttu-id="6fb4b-122">Håndteringen af pluklinjer kan optimeres, hvis der anvendes sorteringskoder, der beskriver de detaljerede oplysninger, som skal bruges til plukning af varer fra lageret, herunder plukrækkefølgen.</span><span class="sxs-lookup"><span data-stu-id="6fb4b-122">Use sort codes to optimize the handling of picking lines, which describe the information that is required for picking items from inventory, including the picking order.</span></span> <span data-ttu-id="6fb4b-123">Sorteringskoder kan angives på basis af lagergangen og andre koordinater, eller de kan tildeles manuelt for en bestemt lokation.</span><span class="sxs-lookup"><span data-stu-id="6fb4b-123">Sort codes can be specified by the aisle and other coordinates, or assigned manually for the location.</span></span>

## <a name="blocked-locations"></a><span data-ttu-id="6fb4b-124">Spærrede lokationer</span><span class="sxs-lookup"><span data-stu-id="6fb4b-124">Blocked locations</span></span>
<span data-ttu-id="6fb4b-125">Det kan ske, at du vil angive en lokation som spærret i en vis periode, f.eks. fordi der skal udføres reparationer.</span><span class="sxs-lookup"><span data-stu-id="6fb4b-125">Occasionally, you might want to indicate that a location is blocked for a period of time, for example, to allow for repairs.</span></span> <span data-ttu-id="6fb4b-126">Det kan også ske, at det kun er nødvendigt at spærre for indlagrings- eller udlagringsstedet.</span><span class="sxs-lookup"><span data-stu-id="6fb4b-126">At other times, you may want to indicate blocking of only the input or only output.</span></span>

## <a name="tree-structure"></a><span data-ttu-id="6fb4b-127">Træstruktur</span><span class="sxs-lookup"><span data-stu-id="6fb4b-127">Tree structure</span></span>

<span data-ttu-id="6fb4b-128">Du kan få vist lagerlayoutet i en træstruktur baseret på koordinaterne for lagerlokationer i et visningsformat på siden Lagerlokationer.</span><span class="sxs-lookup"><span data-stu-id="6fb4b-128">In the Inventory locations page, you can view the warehouse layout in a tree structure based on the coordinates of inventory locations, in a defined display format.</span></span>

## <a name="maintain-inventory-locations-via-the-warehouse-form"></a><span data-ttu-id="6fb4b-129">Vedligehold lagerlokationer via lagerstedsformen</span><span class="sxs-lookup"><span data-stu-id="6fb4b-129">Maintain inventory locations via the warehouse form</span></span>

<span data-ttu-id="6fb4b-130">Det er muligt at kopiere lokationer fra ét lagersted til et andet og oprette steder via en guide.</span><span class="sxs-lookup"><span data-stu-id="6fb4b-130">It is possible to copy locations from one warehouse to another and to create locations via a wizard.</span></span> <span data-ttu-id="6fb4b-131">Inden du kører guiden, skal du kontrollere, at du har defineret standardlokalitetsnavnene på siden Lagersted.</span><span class="sxs-lookup"><span data-stu-id="6fb4b-131">Before you run the wizard you should make sure that you have defined the default location names on the Warehouse page.</span></span>



<a name="additional-resources"></a><span data-ttu-id="6fb4b-132">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="6fb4b-132">Additional resources</span></span>
--------

[<span data-ttu-id="6fb4b-133">Oprette en ny lageropbygning</span><span class="sxs-lookup"><span data-stu-id="6fb4b-133">Create a new warehouse layout</span></span>](tasks/create-new-warehouse-layout.md)
