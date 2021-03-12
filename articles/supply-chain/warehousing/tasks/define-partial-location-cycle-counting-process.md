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
ms.search.form: WHSRFMenuItemCycleCount, WHSCycleCountPlan, WHSCycleCountPlanListPage, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0778cc7c1703dcfd5ea77979aafc99f4f040830d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977132"
---
# <a name="define-partial-location-cycle-counting-process"></a><span data-ttu-id="09391-103">Definere delvis cyklusoptællingsproces for lokalitet</span><span class="sxs-lookup"><span data-stu-id="09391-103">Define partial location cycle counting process</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="09391-104">Når du bruger cyklusoptællingsplaner til at oprette optællingsarbejde, kan du lede de faktiske optællingsoperationer ved at anmode om, at kun specifikke produkter og produktvarianter optælles i stedet for alle disponible lagerbeholdninger på lokationen.</span><span class="sxs-lookup"><span data-stu-id="09391-104">When you use cycle count plans to create counting work, you can guide the actual counting operations by requesting that only specific products and product variants be counted instead of all on-hand inventory at the location.</span></span> <span data-ttu-id="09391-105">Ved at filtrere på bestemte produkter kan lagerchefen reducere evalueringsomkostninger, hjælpe med at forhindre konsolideringsfejl og spare tid.</span><span class="sxs-lookup"><span data-stu-id="09391-105">By filtering on specific products, the warehouse manager can reduce review overhead, help prevent consolidation mistakes, and save time.</span></span> <span data-ttu-id="09391-106">En lagerchef udfører typisk opsætningsopgaver.</span><span class="sxs-lookup"><span data-stu-id="09391-106">Typically, a warehouse manager performs the setup tasks.</span></span> <span data-ttu-id="09391-107">Du kan gennemgå denne procedure i USMF-demodatafirmaet eller i dine egne data.</span><span class="sxs-lookup"><span data-stu-id="09391-107">You can go through this procedure in the USMF demo data company or in your own data.</span></span>


## <a name="create-a-cycle-counting-work-template"></a><span data-ttu-id="09391-108">Oprette en arbejdsskabelon til cyklusoptælling</span><span class="sxs-lookup"><span data-stu-id="09391-108">Create a cycle counting work template</span></span>
1. <span data-ttu-id="09391-109">Gå til Lagerstedsstyring > Opsætning > Arbejde > Arbejdsskabeloner.</span><span class="sxs-lookup"><span data-stu-id="09391-109">Go to Warehouse management > Setup > Work > Work templates.</span></span>
2. <span data-ttu-id="09391-110">Vælg Cyklusoptælling i feltet Arbejdsordretype.</span><span class="sxs-lookup"><span data-stu-id="09391-110">In the Work order type field, select 'Cycle counting'.</span></span>
3. <span data-ttu-id="09391-111">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="09391-111">Click New.</span></span>
4. <span data-ttu-id="09391-112">Indtast et tal i feltet Sekvensnummer.</span><span class="sxs-lookup"><span data-stu-id="09391-112">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="09391-113">Sorteringsrækkefølgen er fra det mindste tal til det største tal.</span><span class="sxs-lookup"><span data-stu-id="09391-113">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="09391-114">Værdien skal være større end 0 (nul).</span><span class="sxs-lookup"><span data-stu-id="09391-114">The value must be more than 0 (zero).</span></span>  
5. <span data-ttu-id="09391-115">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="09391-115">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="09391-116">Indtast en værdi i feltet Arbejdsskabelon.</span><span class="sxs-lookup"><span data-stu-id="09391-116">In the Work template field, type a value.</span></span>
7. <span data-ttu-id="09391-117">Skriv en værdi i feltet Beskrivelse af arbejdsskabelon.</span><span class="sxs-lookup"><span data-stu-id="09391-117">In the Work template description field, type a value.</span></span>
8. <span data-ttu-id="09391-118">Indtast eller vælg en værdi i feltet Arbejdspulje-id.</span><span class="sxs-lookup"><span data-stu-id="09391-118">In the Work pool ID field, enter or select a value.</span></span>
9. <span data-ttu-id="09391-119">Angiv et tal i feltet Arbejdsprioritet.</span><span class="sxs-lookup"><span data-stu-id="09391-119">In the Work priority field, enter a number.</span></span>
10. <span data-ttu-id="09391-120">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="09391-120">Click Save.</span></span>
11. <span data-ttu-id="09391-121">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="09391-121">Click New.</span></span>
12. <span data-ttu-id="09391-122">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="09391-122">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="09391-123">Vælg Optælling i feltet Arbejdstype.</span><span class="sxs-lookup"><span data-stu-id="09391-123">In the Work type field, select 'Counting'.</span></span>
14. <span data-ttu-id="09391-124">Indtast eller vælg en værdi i feltet Arbejdsklasse-id.</span><span class="sxs-lookup"><span data-stu-id="09391-124">In the Work class ID field, enter or select a value.</span></span>
15. <span data-ttu-id="09391-125">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="09391-125">Click Save.</span></span>
16. <span data-ttu-id="09391-126">Klik på Arbejdslinjeskift.</span><span class="sxs-lookup"><span data-stu-id="09391-126">Click Work line breaks.</span></span>
17. <span data-ttu-id="09391-127">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="09391-127">Click New.</span></span>
18. <span data-ttu-id="09391-128">Indtast et tal i feltet Sekvensnummer.</span><span class="sxs-lookup"><span data-stu-id="09391-128">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="09391-129">Sorteringsrækkefølgen er fra det mindste tal til det største tal.</span><span class="sxs-lookup"><span data-stu-id="09391-129">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="09391-130">Værdien skal være større end 0 (nul).</span><span class="sxs-lookup"><span data-stu-id="09391-130">The value must be more than 0 (zero).</span></span>  
19. <span data-ttu-id="09391-131">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="09391-131">Click Save.</span></span>
20. <span data-ttu-id="09391-132">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="09391-132">Close the page.</span></span>
21. <span data-ttu-id="09391-133">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="09391-133">Close the page.</span></span>

## <a name="create-a-cycle-counting-plan"></a><span data-ttu-id="09391-134">Oprette en cyklusoptællingsplan</span><span class="sxs-lookup"><span data-stu-id="09391-134">Create a cycle counting plan</span></span>
1. <span data-ttu-id="09391-135">Gå til Lagerstedsstyring > Opsætning > Cyklusoptælling > Cyklusoptællingsplaner.</span><span class="sxs-lookup"><span data-stu-id="09391-135">Go to Warehouse management > Setup > Cycle counting > Cycle count plans.</span></span>
2. <span data-ttu-id="09391-136">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="09391-136">Click New.</span></span>
3. <span data-ttu-id="09391-137">Skriv en værdi i feltet Id for cyklusoptællingsplan.</span><span class="sxs-lookup"><span data-stu-id="09391-137">In the Cycle counting plan ID field, type a value.</span></span>
4. <span data-ttu-id="09391-138">Indtast en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="09391-138">In the Description field, type a value.</span></span>
5. <span data-ttu-id="09391-139">Angiv et tal i feltet Maks. antal cyklusoptællinger.</span><span class="sxs-lookup"><span data-stu-id="09391-139">In the Maximum number of cycle counts field, enter a number.</span></span>
6. <span data-ttu-id="09391-140">Indtast eller vælg en værdi i feltet Arbejdsskabelon.</span><span class="sxs-lookup"><span data-stu-id="09391-140">In the Work template field, enter or select a value.</span></span>
7. <span data-ttu-id="09391-141">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="09391-141">Click New.</span></span>
8. <span data-ttu-id="09391-142">Indtast et tal i feltet Sekvensnummer.</span><span class="sxs-lookup"><span data-stu-id="09391-142">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="09391-143">Sorteringsrækkefølgen er fra det mindste tal til det største tal.</span><span class="sxs-lookup"><span data-stu-id="09391-143">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="09391-144">Værdien skal være større end 0 (nul).</span><span class="sxs-lookup"><span data-stu-id="09391-144">The value must be more than 0 (zero).</span></span>  
9. <span data-ttu-id="09391-145">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="09391-145">In the Description field, type a value.</span></span>
10. <span data-ttu-id="09391-146">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="09391-146">Click Save.</span></span>
11. <span data-ttu-id="09391-147">Klik på Definer produktforespørgsel.</span><span class="sxs-lookup"><span data-stu-id="09391-147">Click Define product query.</span></span>
12. <span data-ttu-id="09391-148">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="09391-148">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="09391-149">Indtast eller vælg en værdi i feltet Kriterier.</span><span class="sxs-lookup"><span data-stu-id="09391-149">In the Criteria field, enter or select a value.</span></span>
14. <span data-ttu-id="09391-150">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="09391-150">Click OK.</span></span>
15. <span data-ttu-id="09391-151">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="09391-151">Close the page.</span></span>

