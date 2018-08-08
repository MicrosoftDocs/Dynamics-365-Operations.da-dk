--- 
title: "Definere lean planlægningsgrupper"
description: "Lean planlægningsgrupper defineres for at gruppere og adskille produkter i kanban-planlægning."
author: cvocph
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 3ce7185c68b6342c1eae9cc9568da4bf4cc72205
ms.contentlocale: da-dk
ms.lasthandoff: 08/07/2018

---
# <a name="define-lean-schedule-groups"></a><span data-ttu-id="73c85-103">Definere lean planlægningsgrupper</span><span class="sxs-lookup"><span data-stu-id="73c85-103">Define lean schedule groups</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="73c85-104">Lean planlægningsgrupper defineres for at gruppere og adskille produkter i kanban-planlægning.</span><span class="sxs-lookup"><span data-stu-id="73c85-104">Lean schedule groups are defined to group and distinguish products in kanban scheduling.</span></span> <span data-ttu-id="73c85-105">Grupperingen kan foretages som standardtilknytning pr. firma eller som specifik for en arbejdscelle.</span><span class="sxs-lookup"><span data-stu-id="73c85-105">The grouping can be done as generic association per company or specific to a work cell.</span></span> <span data-ttu-id="73c85-106">Hver gruppe har en tildelt farvekode for visuel angivelse i kanban-planlægningens listeside.</span><span class="sxs-lookup"><span data-stu-id="73c85-106">Each group has a color code assigned for visual indication in the kanban scheduling list page.</span></span> <span data-ttu-id="73c85-107">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="73c85-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="define-lean-scheduling-group"></a><span data-ttu-id="73c85-108">Definere lean planlægningsgruppe</span><span class="sxs-lookup"><span data-stu-id="73c85-108">Define lean scheduling group</span></span>
1. <span data-ttu-id="73c85-109">Gå til Administration af produktoplysninger > Lean produktion > Lean planlægningsgrupper.</span><span class="sxs-lookup"><span data-stu-id="73c85-109">Go to Product information management > Lean manufacturing > Lean schedule groups.</span></span>
2. <span data-ttu-id="73c85-110">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="73c85-110">Click New.</span></span>
3. <span data-ttu-id="73c85-111">Indtast en værdi i feltet Planlægningsgruppe.</span><span class="sxs-lookup"><span data-stu-id="73c85-111">In the Schedule group field, type a value.</span></span>
    * <span data-ttu-id="73c85-112">En planlægningsgruppe kan defineres som en global gruppe eller specifik for en arbejdscelle.</span><span class="sxs-lookup"><span data-stu-id="73c85-112">A schedule group can be defined as global group or specific to a work cell.</span></span> <span data-ttu-id="73c85-113">I dette enkle eksempel definerer vi en global gruppe og lader arbejdscellen være tom.</span><span class="sxs-lookup"><span data-stu-id="73c85-113">In this simple example, we define a global group, and the work cell is kept empty.</span></span> <span data-ttu-id="73c85-114">Indstillingerne for denne gruppe gælder for arbejdsceller, der ikke har bestemte planlægningsgrupper.</span><span class="sxs-lookup"><span data-stu-id="73c85-114">The settings of this group apply to all work cells that do not have specific schedule groups.</span></span>  
4. <span data-ttu-id="73c85-115">Vælg en farve i farvevalget.</span><span class="sxs-lookup"><span data-stu-id="73c85-115">Select a color from the color selection.</span></span>
    * <span data-ttu-id="73c85-116">Farverne bruges til at fremhæve job på listesiden for kanban-tidsplanen eller kanban-procesområdet.</span><span class="sxs-lookup"><span data-stu-id="73c85-116">The colors are used to highlight the jobs on the kanban schedule list page or the kanban process board.</span></span>  
5. <span data-ttu-id="73c85-117">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="73c85-117">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="73c85-118">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="73c85-118">In the list, click the link in the selected row.</span></span>

## <a name="associate-product"></a><span data-ttu-id="73c85-119">Tilknytte produkt</span><span class="sxs-lookup"><span data-stu-id="73c85-119">Associate product</span></span>
1. <span data-ttu-id="73c85-120">Tilknytte et bestemt produkt</span><span class="sxs-lookup"><span data-stu-id="73c85-120">Associate a specific product</span></span>
    * <span data-ttu-id="73c85-121">Der er to måder at knytte produkter til lean planlægningsgrupper: enten som et bestemt produkt (varerelationstype = vare) eller som en del af en varefordelingsnøgle (varerelationstype = gruppe).</span><span class="sxs-lookup"><span data-stu-id="73c85-121">There are two ways to associate products to lean schedule groups, either as a specific product (Item relation type = Item) or as part of an item allocation key (item relation type = group).</span></span>    
2. <span data-ttu-id="73c85-122">Vælg Vare i feltet Varerelationstype</span><span class="sxs-lookup"><span data-stu-id="73c85-122">In the Item relation type field, select Item</span></span>
3. <span data-ttu-id="73c85-123">Indtast en værdi i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="73c85-123">In the Item number field, type a value.</span></span>
4. <span data-ttu-id="73c85-124">Angiv et tal i feltet Gennemløbsforhold.</span><span class="sxs-lookup"><span data-stu-id="73c85-124">In the Throughput ratio field, enter a number.</span></span>
    * <span data-ttu-id="73c85-125">Standardgennemløbsforholdet er 1, hvilket betyder, at de relaterede produkter forbruger nøjagtigt den kapacitet, der er angivet i procesaktiviteterne for produktionsflowene.</span><span class="sxs-lookup"><span data-stu-id="73c85-125">The default Throughput ratio is 1, which means that the related products consume exactly the capacity specified in the process activities of the production flows.</span></span> <span data-ttu-id="73c85-126">Gennemløbsforhold > 1 definerer et højere ressourceforbrug, Gennemløbsforhold < 1 definerer et lavere ressourceforbrug.</span><span class="sxs-lookup"><span data-stu-id="73c85-126">Throughput ratio > 1 defines a higher resource consumption, Throughput ratio < 1 defines a lower resource consumption.</span></span> <span data-ttu-id="73c85-127">Forholdet bruges i omkostningsberegningen og i beregningen af kanban-jobforbruget.</span><span class="sxs-lookup"><span data-stu-id="73c85-127">The ratio is used in the cost calculation and in the calculation of the kanban job consumption.</span></span>  

## <a name="associate-item-allocation-key"></a><span data-ttu-id="73c85-128">Tilknytte varefordelingsnøgle</span><span class="sxs-lookup"><span data-stu-id="73c85-128">Associate item allocation key</span></span>
1. <span data-ttu-id="73c85-129">Tilknytte en varefordelingsnøgle</span><span class="sxs-lookup"><span data-stu-id="73c85-129">Associate an item allocation key</span></span>
    * <span data-ttu-id="73c85-130">Føj en tilknytning til en varefordelingsnøgle ved hjælp af varerelationstypen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="73c85-130">Add an association to an item allocation key by using the Item relation type Group.</span></span>   <span data-ttu-id="73c85-131">Bemærk, at denne proces skal du en budgetvarefordelingsnøgle, der er defineret i dataene.</span><span class="sxs-lookup"><span data-stu-id="73c85-131">Note that for this process, you need a forecast item allocation key defined in your data.</span></span>  
2. <span data-ttu-id="73c85-132">Vælg Gruppe i feltet Varerelationstype</span><span class="sxs-lookup"><span data-stu-id="73c85-132">In the Item relation type field, select Group</span></span>
3. <span data-ttu-id="73c85-133">Klik på rullelisten i feltet Varefordelingsnøgle for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="73c85-133">In the Item allocation key field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="73c85-134">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="73c85-134">In the list, click the link in the selected row.</span></span>


