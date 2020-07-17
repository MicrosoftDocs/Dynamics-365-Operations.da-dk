---
title: Konfigurere vareomfordeling for kort plukning
description: Dette emner viser, hvordan du giver lagermedarbejderne mulighed for hurtigt at finde alternative lokaliteter, hvis der ikke er tilstrækkeligt lager på den lokation, der er blevet henvist til.
author: ShylaThompson
manager: tfehr
ms.date: 06/29/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkException, WHSWorker
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e14a4fc72d256bea31296bff80d5b5818b95ea9d
ms.sourcegitcommit: ce397c2759f642c595e30fef58a770b50360b2bd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/01/2020
ms.locfileid: "3527413"
---
# <a name="set-up-short-picking-item-reallocation"></a><span data-ttu-id="ee3df-103">Konfigurere vareomfordeling for kort plukning</span><span class="sxs-lookup"><span data-stu-id="ee3df-103">Set up short picking item reallocation</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ee3df-104">Denne fremgangsmåde viser, hvordan du giver lagermedarbejderne mulighed for hurtigt at finde alternative lokationer, hvis der ikke er tilstrækkeligt lager på den lokation, der er blevet henvist til.</span><span class="sxs-lookup"><span data-stu-id="ee3df-104">This procedure shows how to enable warehouse workers to quickly find alternative locations if there isn’t sufficient inventory at the location they’ve been directed to.</span></span> 

<span data-ttu-id="ee3df-105">Omfordelingsprocessen styres af en **Arbejdsundtagelse** og bruges af **lagermedarbejderen.**</span><span class="sxs-lookup"><span data-stu-id="ee3df-105">The reallocation process is controlled by a **Work exception** and used by the warehouse **worker.**</span></span>

<span data-ttu-id="ee3df-106">Det er muligt at bruge automatiske, manuelle eller begge omfordelingsprocesser:</span><span class="sxs-lookup"><span data-stu-id="ee3df-106">It is possible to use Automatic, Manual, or both reallocation processes:</span></span>

- <span data-ttu-id="ee3df-107">Automatisk omfordeling – lokationsvejledninger bruges til at bestemme, om varerne er tilgængelige på en anden lokation.</span><span class="sxs-lookup"><span data-stu-id="ee3df-107">Automatic reallocation - Location directives are used to determine if the goods are available at another location.</span></span> <span data-ttu-id="ee3df-108">Hvis det er muligt, opdateres arbejdet, og lagerbrugeren dirigeres videre til den alternative lokation.</span><span class="sxs-lookup"><span data-stu-id="ee3df-108">If possible, the work will be updated and the warehouse user will be directed to the alternative location.</span></span>
- <span data-ttu-id="ee3df-109">Manuel omfordeling – gør det muligt for lagerbrugeren at vælge mellem en eller flere lokationer med ikke-reserverede antal varer.</span><span class="sxs-lookup"><span data-stu-id="ee3df-109">Manual reallocation - Allows the warehouse user to select from one or more locations with unreserved quantities of goods.</span></span> 
- <span data-ttu-id="ee3df-110">Automatisk og manuel – hvis systemet ikke kan udføre en automatisk omfordeling, og der er tilgængelige lokationer med ikke-reserverede antal, vil brugeren blive bedt om at vælge en lokalitet.</span><span class="sxs-lookup"><span data-stu-id="ee3df-110">Automatic and manual - If the system is unable to perform an automatic reallocation, and locations are available with unreserved quantities, the user will be prompted to select a location.</span></span>

## <a name="set-up-work-exceptions"></a><span data-ttu-id="ee3df-111">Konfigurer arbejdsundtagelser</span><span class="sxs-lookup"><span data-stu-id="ee3df-111">Set up work exceptions</span></span>
<span data-ttu-id="ee3df-112">Det er muligt at definere flere undtagelser for arbejde med forskellige politikker for omfordeling af varer for at give lagermedarbejderen mulighed for at vælge én baseret på behov i den leverance, som de behandler.</span><span class="sxs-lookup"><span data-stu-id="ee3df-112">It's possible to define several work exceptions with different item reallocation policies to enable the warehouse worker to choose one based on the needs of the shipment that they are processing.</span></span>

<span data-ttu-id="ee3df-113">Demodatafirmaet USMF bruges til at oprette denne procedure.</span><span class="sxs-lookup"><span data-stu-id="ee3df-113">The USMF demo data company was used to create this procedure.</span></span>

1. <span data-ttu-id="ee3df-114">I **Navigationsrude** skal du gå til **Lokationsstyring > Opsætning > Arbejde > Arbejdsundtagelser**.</span><span class="sxs-lookup"><span data-stu-id="ee3df-114">In the **Navigation pane**, go to **Warehouse management > Setup > Work > Work exceptions**.</span></span>
2. <span data-ttu-id="ee3df-115">Klik på **Ny**</span><span class="sxs-lookup"><span data-stu-id="ee3df-115">Click **New**</span></span> 
3. <span data-ttu-id="ee3df-116">Indtast en værdi i feltet **Kode for arbejdsundtagelse**.</span><span class="sxs-lookup"><span data-stu-id="ee3df-116">In the **Work exception code** field, type a value.</span></span> <span data-ttu-id="ee3df-117">Dette vil være titlen på denne undtagelse.</span><span class="sxs-lookup"><span data-stu-id="ee3df-117">This will be the title of this exception .</span></span> <span data-ttu-id="ee3df-118">Det kan f.eks. være Vejledning til korte pluk.</span><span class="sxs-lookup"><span data-stu-id="ee3df-118">For example, Short picking manual.</span></span>
4. <span data-ttu-id="ee3df-119">Indtast en værdi i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="ee3df-119">In the **Description** field, type a value.</span></span> <span data-ttu-id="ee3df-120">Dette er en kort beskrivelse af brugen af denne undtagelse.</span><span class="sxs-lookup"><span data-stu-id="ee3df-120">This will be a short description of the usage of this exception.</span></span> <span data-ttu-id="ee3df-121">Elementet Kort pluk er f. eks. ikke tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="ee3df-121">For example, Short picking - item not available.</span></span>
5. <span data-ttu-id="ee3df-122">Vælg **Kort pluk** i feltet **Undtagelsestype**.</span><span class="sxs-lookup"><span data-stu-id="ee3df-122">In the **Exception** type field, select **Short pick**.</span></span>
6. <span data-ttu-id="ee3df-123">Marker afkrydsningsfeltet **Reguler lager**.</span><span class="sxs-lookup"><span data-stu-id="ee3df-123">Select the **Adjust inventory** check box.</span></span> <span data-ttu-id="ee3df-124">Hvis indstillingen er valg, reguleres lageret automatisk til 0 på den lokation, hvor der er udført korte pluk.</span><span class="sxs-lookup"><span data-stu-id="ee3df-124">If selected, inventory will automatically be adjusted to 0 at the short picked location.</span></span>
7. <span data-ttu-id="ee3df-125">Indtast eller vælg en værdi i feltet **Standardkode for reguleringstype**.</span><span class="sxs-lookup"><span data-stu-id="ee3df-125">In the **Default adjustment type code** field, enter or select a value.</span></span> <span data-ttu-id="ee3df-126">I USMF kan du f.eks. vælge **Fjern Res Adj Out**. Hver reguleringstypekode indeholder fire karakteristika: navn, beskrivelse, lagerkladdenavn og **Fjern reservationer**.</span><span class="sxs-lookup"><span data-stu-id="ee3df-126">For example, in USMF you can select **Remove Res Adj Out**. Each Adjustment type code contains four characteristics: name, description, inventory journal name, and **Remove reservations**.</span></span> <span data-ttu-id="ee3df-127">Hvis **Fjern reservationer** er aktiveret, vil reservationerne for ordrelinjer med kort pluk blive fjernet.</span><span class="sxs-lookup"><span data-stu-id="ee3df-127">If **Remove reservations** is enabled, the short-picked order line's reservations will be removed.</span></span>  
8. <span data-ttu-id="ee3df-128">Vælg en værdi i feltet **Vareomfordeling** som f.eks. Manuel.</span><span class="sxs-lookup"><span data-stu-id="ee3df-128">In the **Item reallocation** field, select a value, such as Manual.</span></span> <span data-ttu-id="ee3df-129">Hvis du vælger Manuel eller Automatisk og manuel, skal lagermedarbejderen have mulighed for at bruge manuel omfordeling.</span><span class="sxs-lookup"><span data-stu-id="ee3df-129">If you select Manual, or Automatic and Manual, the warehouse worker needs to be enabled to use manual reallocation.</span></span>

## <a name="set-up-a-worker-to-use-manual-item-reallocation"></a><span data-ttu-id="ee3df-130">Konfigurer en arbejder til at bruge manuel vareomfordeling</span><span class="sxs-lookup"><span data-stu-id="ee3df-130">Set up a worker to use manual item reallocation</span></span>

<span data-ttu-id="ee3df-131">Demodatafirmaet USMF bruges til at oprette denne procedure.</span><span class="sxs-lookup"><span data-stu-id="ee3df-131">The USMF demo data company was used to create this procedure.</span></span>

1. <span data-ttu-id="ee3df-132">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="ee3df-132">Close the page.</span></span>
2. <span data-ttu-id="ee3df-133">I **Navigationsrude** skal du gå til **Lokationsstyring > Opsætning > Arbejder**.</span><span class="sxs-lookup"><span data-stu-id="ee3df-133">In the **Navigation pane**, go to **Warehouse management > Setup > Worker**.</span></span>
3. <span data-ttu-id="ee3df-134">Klik på **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="ee3df-134">Click **Edit**.</span></span>
4. <span data-ttu-id="ee3df-135">Vælg arbejder på listen.</span><span class="sxs-lookup"><span data-stu-id="ee3df-135">In the list, select worker.</span></span> <span data-ttu-id="ee3df-136">F.eks. Julia Funderburk.</span><span class="sxs-lookup"><span data-stu-id="ee3df-136">For example, Julia Funderburk.</span></span>
5. <span data-ttu-id="ee3df-137">Udvid oversigtspanelet **Brugere**.</span><span class="sxs-lookup"><span data-stu-id="ee3df-137">Expand the **Users** FastTab.</span></span>
6. <span data-ttu-id="ee3df-138">Vælg et **bruger-id** på listen.</span><span class="sxs-lookup"><span data-stu-id="ee3df-138">In the list, select a **User ID**.</span></span> <span data-ttu-id="ee3df-139">For eksempel 24.</span><span class="sxs-lookup"><span data-stu-id="ee3df-139">For example, 24.</span></span>
7. <span data-ttu-id="ee3df-140">Udvid oversigtspanelet **Arbejde**.</span><span class="sxs-lookup"><span data-stu-id="ee3df-140">Expand the **Work** FastTab.</span></span>
8. <span data-ttu-id="ee3df-141">Vælg **Ja** i feltet **Tillad manuel vareomfordeling**.</span><span class="sxs-lookup"><span data-stu-id="ee3df-141">Select **Yes** in the **Allow manual item reallocation** field.</span></span>
