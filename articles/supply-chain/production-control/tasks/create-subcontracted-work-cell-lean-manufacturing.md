--- 
title: "Oprette en underleverandørarbejdscelle for lean manufacturing"
description: "Hvis du vil tilpasse underleverandørarbejde for lean manufacturing, skal du oprette en arbejdscelle, der er tilknyttet den kreditor, der leverer arbejdet."
author: cvocph
manager: AnnBe
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: fc8dc0bc29c6bdb662c46808491abf5395f0be5d
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-subcontracted-work-cell-for-lean-manufacturing"></a><span data-ttu-id="f8f94-103">Oprette en underleverandørarbejdscelle for lean manufacturing</span><span class="sxs-lookup"><span data-stu-id="f8f94-103">Create a subcontracted work cell for lean manufacturing</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f8f94-104">Hvis du vil tilpasse underleverandørarbejde for lean manufacturing, skal du oprette en arbejdscelle, der er tilknyttet den kreditor, der leverer arbejdet.</span><span class="sxs-lookup"><span data-stu-id="f8f94-104">To model subcontracted work for lean manufacturing, you must create a work cell that is associated with the vendor that provides the work.</span></span> <span data-ttu-id="f8f94-105">En underleverandørarbejdscelle er knyttet til kreditoren gennem tilknytningen af en ressource af typen Kreditor.</span><span class="sxs-lookup"><span data-stu-id="f8f94-105">A subcontracted work cell is linked to the vendor through the association of a resource of the Vendor type.</span></span> <span data-ttu-id="f8f94-106">Hvis du afspiller denne optagelse i USMF-demofirmaet, kan du vælge kreditorkonto-ID'et 1002 og lokation 1.</span><span class="sxs-lookup"><span data-stu-id="f8f94-106">If you play this recording in the USMF demo company, you can select vendor account ID 1002 and site 1.</span></span>


## <a name="create-a-vendor-resource"></a><span data-ttu-id="f8f94-107">Oprette en leverandørressource</span><span class="sxs-lookup"><span data-stu-id="f8f94-107">Create a vendor resource</span></span>
1. <span data-ttu-id="f8f94-108">Gå til ressourcer.</span><span class="sxs-lookup"><span data-stu-id="f8f94-108">Go to Resources.</span></span>
2. <span data-ttu-id="f8f94-109">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="f8f94-109">Click New.</span></span>
3. <span data-ttu-id="f8f94-110">Skriv en værdi i feltet Ressource.</span><span class="sxs-lookup"><span data-stu-id="f8f94-110">In the Resource field, type a value.</span></span>
4. <span data-ttu-id="f8f94-111">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="f8f94-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="f8f94-112">Vælg Kreditor i feltet Type.</span><span class="sxs-lookup"><span data-stu-id="f8f94-112">In the Type field, select 'Vendor'.</span></span>
6. <span data-ttu-id="f8f94-113">Klik på rullelisten i feltet Kreditor for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="f8f94-113">In the Vendor field, click the drop-down button to open the lookup.</span></span>

## <a name="create-the-resource-group"></a><span data-ttu-id="f8f94-114">Oprette ressourcegruppen</span><span class="sxs-lookup"><span data-stu-id="f8f94-114">Create the resource group</span></span>
1. <span data-ttu-id="f8f94-115">Gå til Ressourcegrupper.</span><span class="sxs-lookup"><span data-stu-id="f8f94-115">Go to Resource groups.</span></span>
2. <span data-ttu-id="f8f94-116">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="f8f94-116">Click New.</span></span>
3. <span data-ttu-id="f8f94-117">Indtast en værdi i feltet Ressourcegruppe.</span><span class="sxs-lookup"><span data-stu-id="f8f94-117">In the Resource group field, type a value.</span></span>
4. <span data-ttu-id="f8f94-118">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="f8f94-118">In the Description field, type a value.</span></span>
5. <span data-ttu-id="f8f94-119">Klik på rullelisten i feltet Sted for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="f8f94-119">In the Site field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f8f94-120">Vælg det sted, som arbejdscellen skal tildeles til.</span><span class="sxs-lookup"><span data-stu-id="f8f94-120">Select the site that the work cell should be allocated to.</span></span> <span data-ttu-id="f8f94-121">I teorien kan et sted repræsentere et enkelt sted, der styres af en leverandør.</span><span class="sxs-lookup"><span data-stu-id="f8f94-121">In theory, a site can represent a single site that is operated by a vendor.</span></span> <span data-ttu-id="f8f94-122">I de fleste tilfælde tildeles underleverandørressourcer kun til det sted, der bestiller underleverandørarbejdet.</span><span class="sxs-lookup"><span data-stu-id="f8f94-122">However, in most cases, subcontracted resources are just allocated to the site that orders the subcontracted work.</span></span> <span data-ttu-id="f8f94-123">Bemærk, at ind- og udlageringsstederne for arbejde udført af underleverandørens arbejdsceller skal være samme sted.</span><span class="sxs-lookup"><span data-stu-id="f8f94-123">Note that the input and output warehouses of subcontracted work cells must be on the same site.</span></span>  
6. <span data-ttu-id="f8f94-124">Skriv en værdi i feltet Sted.</span><span class="sxs-lookup"><span data-stu-id="f8f94-124">In the Site field, type a value.</span></span>
7. @SysTaskRecorder:_RequestClose
8. <span data-ttu-id="f8f94-125">Markér eller fjern markeringen i afkrydsningsfeltet Arbejdscelle.</span><span class="sxs-lookup"><span data-stu-id="f8f94-125">Select or clear the Work cell check box.</span></span>
9. <span data-ttu-id="f8f94-126">Klik på rullelisten i feltet Indlagringssted for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="f8f94-126">In the Input warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f8f94-127">Vælg det lagersted og lokalitet, der bruges til at forberede materialer til den kreditoradministrerede arbejdscelle.</span><span class="sxs-lookup"><span data-stu-id="f8f94-127">Select the warehouse and location that are used to stage the material for the vendor-managed work cell.</span></span> <span data-ttu-id="f8f94-128">I mange tilfælde tilpasses lagerstedet og lokaliteten ved hjælp af et separat lagersted pr. leverandør og én lokalitet pr. arbejdscelle.</span><span class="sxs-lookup"><span data-stu-id="f8f94-128">In many cases, the warehouse and location are modeled by using a separate warehouse per vendor and one location per work cell.</span></span>  
10. <span data-ttu-id="f8f94-129">Klik på rullelisten i feltet Indlagringslokation for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="f8f94-129">In the Input location field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="f8f94-130">Klik på rullelisten i feltet Udlagringssteder for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="f8f94-130">In the Output warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f8f94-131">Angiv det lagersted og lokalitet, hvor materialet bogføres, når underleverandørens aktiviteter for arbejdscellen bogføres.</span><span class="sxs-lookup"><span data-stu-id="f8f94-131">Define the warehouse and location where the material is posted when the subcontracted activities of the work cell are posted.</span></span> <span data-ttu-id="f8f94-132">Lagerstedet og lokaliteten kan være på leverandørens lokalitet, hvis leverandøren rapporterer kanban-job.</span><span class="sxs-lookup"><span data-stu-id="f8f94-132">The warehouse and location can be at the vendor site if the vendor reports the kanban jobs.</span></span> <span data-ttu-id="f8f94-133">Lagerstedet og lokaliteten kan også være den modtagende lokalitet, der er knyttet til det næste trin i produktionsflowet.</span><span class="sxs-lookup"><span data-stu-id="f8f94-133">Alternatively, the warehouse and location can be the receiving location that is associated with the next step of the production flow.</span></span>  
12. <span data-ttu-id="f8f94-134">Klik på rullelisten i feltet Udlagringslokation for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="f8f94-134">In the Output location field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="f8f94-135">Udvid eller skjul sektionen Kalendere.</span><span class="sxs-lookup"><span data-stu-id="f8f94-135">Expand or collapse the Calendars section.</span></span>
14. <span data-ttu-id="f8f94-136">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="f8f94-136">Click Add.</span></span>
15. <span data-ttu-id="f8f94-137">Klik på rullelisten i feltet Kalender for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="f8f94-137">In the Calendar field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f8f94-138">Knyt arbejdstidskalenderen for arbejdscellen til ressourcegruppen.</span><span class="sxs-lookup"><span data-stu-id="f8f94-138">Associate the working time calendar of the work cell with the resource group.</span></span> <span data-ttu-id="f8f94-139">Det anbefales, at du for vigtige ressourcer definerer bestemte kalendere, der repræsenterer de nøjagtige arbejdstider og relateret kapacitet for arbejdscellen eller leverandørlokaliteten.</span><span class="sxs-lookup"><span data-stu-id="f8f94-139">For critical resources, we recommend that you define specific calendars that represent the exact working times and related capacities of the work cell or vendor site.</span></span>  
16. <span data-ttu-id="f8f94-140">Udvid eller skjul sektionen Ressourcer.</span><span class="sxs-lookup"><span data-stu-id="f8f94-140">Expand or collapse the Resources section.</span></span>
17. <span data-ttu-id="f8f94-141">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="f8f94-141">Click Add.</span></span>
    * <span data-ttu-id="f8f94-142">En underleverandørressourcegruppe skal have en tilknyttet ressource af typen Leverandør, der knytter ressourcegruppen til kreditorkontoen.</span><span class="sxs-lookup"><span data-stu-id="f8f94-142">A subcontracted resource group must have an associated resource of the Vendor type that links the resource group to the vendor account.</span></span>  
18. <span data-ttu-id="f8f94-143">Klik på rullelisten i feltet Ressource for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="f8f94-143">In the Resource field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f8f94-144">Vælg eller angiv den leverandørressource, du oprettede i forrige underopgave.</span><span class="sxs-lookup"><span data-stu-id="f8f94-144">Select or enter the vendor resource that you created in the previous sub-task.</span></span>  
19. <span data-ttu-id="f8f94-145">Udvid eller skjul afsnittet Arbejdscelles kapacitet.</span><span class="sxs-lookup"><span data-stu-id="f8f94-145">Expand or collapse the Work cell capacity section.</span></span>
20. <span data-ttu-id="f8f94-146">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="f8f94-146">Click Add.</span></span>
    * <span data-ttu-id="f8f94-147">En arbejdscelle skal have en defineret kapacitet.</span><span class="sxs-lookup"><span data-stu-id="f8f94-147">A work cell must have a defined capacity.</span></span> <span data-ttu-id="f8f94-148">I dette eksempel skal vi oprette en gennemløbskapacitet på 100 styk pr. standardarbejdsdag.</span><span class="sxs-lookup"><span data-stu-id="f8f94-148">In this example, we create a throughput capacity of 100 pieces per standard workday.</span></span>  
21. <span data-ttu-id="f8f94-149">Klik på rullelisten i feltet Produktionsflowmodel for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="f8f94-149">In the Production flow model field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="f8f94-150">Vælg en indstilling i feltet Kapacitetsperiode.</span><span class="sxs-lookup"><span data-stu-id="f8f94-150">In the Capacity period field, select an option.</span></span>
23. <span data-ttu-id="f8f94-151">Indtast et tal i feltet Gennemsnitligt antal gennemløb.</span><span class="sxs-lookup"><span data-stu-id="f8f94-151">In the Average throughput quantity field, enter a number.</span></span>
24. <span data-ttu-id="f8f94-152">Klik på rullelisten i feltet Enhed for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="f8f94-152">In the Unit field, click the drop-down button to open the lookup.</span></span>
25. <span data-ttu-id="f8f94-153">ResolveChanges enheden.</span><span class="sxs-lookup"><span data-stu-id="f8f94-153">ResolveChanges the Unit.</span></span>


