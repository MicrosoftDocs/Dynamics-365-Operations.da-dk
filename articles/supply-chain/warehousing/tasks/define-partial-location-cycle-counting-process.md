---
title: Definere delvis cyklusoptællingsproces for lokalitet
description: Når du bruger cyklusoptællingsplaner til at oprette optællingsarbejde, kan du lede de faktiske optællingsoperationer ved at anmode om, at kun specifikke produkter og produktvarianter optælles i stedet for alle disponible lagerbeholdninger på lokationen.
author: ShylaThompson
manager: tfehr
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3d80171ec524e3401d7971cb743d73abdda87ff
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3217028"
---
# <a name="define-partial-location-cycle-counting-process"></a><span data-ttu-id="12968-103">Definere delvis cyklusoptællingsproces for lokalitet</span><span class="sxs-lookup"><span data-stu-id="12968-103">Define partial location cycle counting process</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="12968-104">Når du bruger cyklusoptællingsplaner til at oprette optællingsarbejde, kan du lede de faktiske optællingsoperationer ved at anmode om, at kun specifikke produkter og produktvarianter optælles i stedet for alle disponible lagerbeholdninger på lokationen.</span><span class="sxs-lookup"><span data-stu-id="12968-104">When you use cycle count plans to create counting work, you can guide the actual counting operations by requesting that only specific products and product variants be counted instead of all on-hand inventory at the location.</span></span> <span data-ttu-id="12968-105">Ved at filtrere på bestemte produkter kan lagerchefen reducere evalueringsomkostninger, hjælpe med at forhindre konsolideringsfejl og spare tid.</span><span class="sxs-lookup"><span data-stu-id="12968-105">By filtering on specific products, the warehouse manager can reduce review overhead, help prevent consolidation mistakes, and save time.</span></span> <span data-ttu-id="12968-106">En lagerchef udfører typisk opsætningsopgaver.</span><span class="sxs-lookup"><span data-stu-id="12968-106">Typically, a warehouse manager performs the setup tasks.</span></span> <span data-ttu-id="12968-107">Du kan gennemgå denne procedure i USMF-demodatafirmaet eller i dine egne data.</span><span class="sxs-lookup"><span data-stu-id="12968-107">You can go through this procedure in the USMF demo data company or in your own data.</span></span>


## <a name="create-a-cycle-counting-work-template"></a><span data-ttu-id="12968-108">Oprette en arbejdsskabelon til cyklusoptælling</span><span class="sxs-lookup"><span data-stu-id="12968-108">Create a cycle counting work template</span></span>
1. <span data-ttu-id="12968-109">Gå til Lagerstedsstyring > Opsætning > Arbejde > Arbejdsskabeloner.</span><span class="sxs-lookup"><span data-stu-id="12968-109">Go to Warehouse management > Setup > Work > Work templates.</span></span>
2. <span data-ttu-id="12968-110">Vælg Cyklusoptælling i feltet Arbejdsordretype.</span><span class="sxs-lookup"><span data-stu-id="12968-110">In the Work order type field, select 'Cycle counting'.</span></span>
3. <span data-ttu-id="12968-111">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="12968-111">Click New.</span></span>
4. <span data-ttu-id="12968-112">Indtast et tal i feltet Sekvensnummer.</span><span class="sxs-lookup"><span data-stu-id="12968-112">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="12968-113">Sorteringsrækkefølgen er fra det mindste tal til det største tal.</span><span class="sxs-lookup"><span data-stu-id="12968-113">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="12968-114">Værdien skal være større end 0 (nul).</span><span class="sxs-lookup"><span data-stu-id="12968-114">The value must be more than 0 (zero).</span></span>  
5. <span data-ttu-id="12968-115">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="12968-115">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="12968-116">Indtast en værdi i feltet Arbejdsskabelon.</span><span class="sxs-lookup"><span data-stu-id="12968-116">In the Work template field, type a value.</span></span>
7. <span data-ttu-id="12968-117">Skriv en værdi i feltet Beskrivelse af arbejdsskabelon.</span><span class="sxs-lookup"><span data-stu-id="12968-117">In the Work template description field, type a value.</span></span>
8. <span data-ttu-id="12968-118">Indtast eller vælg en værdi i feltet Arbejdspulje-id.</span><span class="sxs-lookup"><span data-stu-id="12968-118">In the Work pool ID field, enter or select a value.</span></span>
9. <span data-ttu-id="12968-119">Angiv et tal i feltet Arbejdsprioritet.</span><span class="sxs-lookup"><span data-stu-id="12968-119">In the Work priority field, enter a number.</span></span>
10. <span data-ttu-id="12968-120">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="12968-120">Click Save.</span></span>
11. <span data-ttu-id="12968-121">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="12968-121">Click New.</span></span>
12. <span data-ttu-id="12968-122">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="12968-122">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="12968-123">Vælg Optælling i feltet Arbejdstype.</span><span class="sxs-lookup"><span data-stu-id="12968-123">In the Work type field, select 'Counting'.</span></span>
14. <span data-ttu-id="12968-124">Indtast eller vælg en værdi i feltet Arbejdsklasse-id.</span><span class="sxs-lookup"><span data-stu-id="12968-124">In the Work class ID field, enter or select a value.</span></span>
15. <span data-ttu-id="12968-125">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="12968-125">Click Save.</span></span>
16. <span data-ttu-id="12968-126">Klik på Arbejdslinjeskift.</span><span class="sxs-lookup"><span data-stu-id="12968-126">Click Work line breaks.</span></span>
17. <span data-ttu-id="12968-127">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="12968-127">Click New.</span></span>
18. <span data-ttu-id="12968-128">Indtast et tal i feltet Sekvensnummer.</span><span class="sxs-lookup"><span data-stu-id="12968-128">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="12968-129">Sorteringsrækkefølgen er fra det mindste tal til det største tal.</span><span class="sxs-lookup"><span data-stu-id="12968-129">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="12968-130">Værdien skal være større end 0 (nul).</span><span class="sxs-lookup"><span data-stu-id="12968-130">The value must be more than 0 (zero).</span></span>  
19. <span data-ttu-id="12968-131">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="12968-131">Click Save.</span></span>
20. <span data-ttu-id="12968-132">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="12968-132">Close the page.</span></span>
21. <span data-ttu-id="12968-133">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="12968-133">Close the page.</span></span>

## <a name="create-a-cycle-counting-plan"></a><span data-ttu-id="12968-134">Oprette en cyklusoptællingsplan</span><span class="sxs-lookup"><span data-stu-id="12968-134">Create a cycle counting plan</span></span>
1. <span data-ttu-id="12968-135">Gå til Lagerstedsstyring > Opsætning > Cyklusoptælling > Cyklusoptællingsplaner.</span><span class="sxs-lookup"><span data-stu-id="12968-135">Go to Warehouse management > Setup > Cycle counting > Cycle count plans.</span></span>
2. <span data-ttu-id="12968-136">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="12968-136">Click New.</span></span>
3. <span data-ttu-id="12968-137">Skriv en værdi i feltet Id for cyklusoptællingsplan.</span><span class="sxs-lookup"><span data-stu-id="12968-137">In the Cycle counting plan ID field, type a value.</span></span>
4. <span data-ttu-id="12968-138">Indtast en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="12968-138">In the Description field, type a value.</span></span>
5. <span data-ttu-id="12968-139">Angiv et tal i feltet Maks. antal cyklusoptællinger.</span><span class="sxs-lookup"><span data-stu-id="12968-139">In the Maximum number of cycle counts field, enter a number.</span></span>
6. <span data-ttu-id="12968-140">Indtast eller vælg en værdi i feltet Arbejdsskabelon.</span><span class="sxs-lookup"><span data-stu-id="12968-140">In the Work template field, enter or select a value.</span></span>
7. <span data-ttu-id="12968-141">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="12968-141">Click New.</span></span>
8. <span data-ttu-id="12968-142">Indtast et tal i feltet Sekvensnummer.</span><span class="sxs-lookup"><span data-stu-id="12968-142">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="12968-143">Sorteringsrækkefølgen er fra det mindste tal til det største tal.</span><span class="sxs-lookup"><span data-stu-id="12968-143">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="12968-144">Værdien skal være større end 0 (nul).</span><span class="sxs-lookup"><span data-stu-id="12968-144">The value must be more than 0 (zero).</span></span>  
9. <span data-ttu-id="12968-145">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="12968-145">In the Description field, type a value.</span></span>
10. <span data-ttu-id="12968-146">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="12968-146">Click Save.</span></span>
11. <span data-ttu-id="12968-147">Klik på Definer produktforespørgsel.</span><span class="sxs-lookup"><span data-stu-id="12968-147">Click Define product query.</span></span>
12. <span data-ttu-id="12968-148">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="12968-148">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="12968-149">Indtast eller vælg en værdi i feltet Kriterier.</span><span class="sxs-lookup"><span data-stu-id="12968-149">In the Criteria field, enter or select a value.</span></span>
14. <span data-ttu-id="12968-150">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="12968-150">Click OK.</span></span>
15. <span data-ttu-id="12968-151">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="12968-151">Close the page.</span></span>

