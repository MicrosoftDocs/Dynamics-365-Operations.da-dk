---
title: Definere lean planlægningsgrupper
description: Lean planlægningsgrupper defineres for at gruppere og adskille produkter i kanban-planlægning.
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanScheduleGroup, GanttColorTableLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a9ad470d81d94a0af1c4c4dc6c5072354cfd96d2
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/10/2020
ms.locfileid: "3975842"
---
# <a name="define-lean-schedule-groups"></a><span data-ttu-id="c15d9-103">Definere lean planlægningsgrupper</span><span class="sxs-lookup"><span data-stu-id="c15d9-103">Define lean schedule groups</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c15d9-104">Lean planlægningsgrupper defineres for at gruppere og adskille produkter i kanban-planlægning.</span><span class="sxs-lookup"><span data-stu-id="c15d9-104">Lean schedule groups are defined to group and distinguish products in kanban scheduling.</span></span> <span data-ttu-id="c15d9-105">Grupperingen kan foretages som standardtilknytning pr. firma eller som specifik for en arbejdscelle.</span><span class="sxs-lookup"><span data-stu-id="c15d9-105">The grouping can be done as generic association per company or specific to a work cell.</span></span> <span data-ttu-id="c15d9-106">Hver gruppe har en tildelt farvekode for visuel angivelse i kanban-planlægningens listpage.</span><span class="sxs-lookup"><span data-stu-id="c15d9-106">Each group has a color code assigned for visual indication in the kanban scheduling listpage.</span></span> <span data-ttu-id="c15d9-107">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="c15d9-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="define-lean-scheduling-group"></a><span data-ttu-id="c15d9-108">Definere lean planlægningsgruppe</span><span class="sxs-lookup"><span data-stu-id="c15d9-108">Define lean scheduling group</span></span>
1. <span data-ttu-id="c15d9-109">Gå til Administration af produktoplysninger > Lean produktion > Lean planlægningsgrupper.</span><span class="sxs-lookup"><span data-stu-id="c15d9-109">Go to Product information management > Lean manufacturing > Lean schedule groups.</span></span>
2. <span data-ttu-id="c15d9-110">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="c15d9-110">Click New.</span></span>
3. <span data-ttu-id="c15d9-111">Indtast en værdi i feltet Planlægningsgruppe.</span><span class="sxs-lookup"><span data-stu-id="c15d9-111">In the Schedule group field, type a value.</span></span>
    * <span data-ttu-id="c15d9-112">En planlægningsgruppe kan defineres som en global gruppe eller specifik for en arbejdscelle.</span><span class="sxs-lookup"><span data-stu-id="c15d9-112">A schedule group can be defined as global group or specific to a work cell.</span></span> <span data-ttu-id="c15d9-113">I dette enkle eksempel definerer vi en global gruppe og lader arbejdscellen være tom.</span><span class="sxs-lookup"><span data-stu-id="c15d9-113">In this simple example, we define a global group, and the work cell is kept empty.</span></span> <span data-ttu-id="c15d9-114">Indstillingerne for denne gruppe gælder for arbejdsceller, der ikke har bestemte planlægningsgrupper.</span><span class="sxs-lookup"><span data-stu-id="c15d9-114">The settings of this group apply to all work cells that do not have specific schedule groups.</span></span>  
4. <span data-ttu-id="c15d9-115">Vælg en farve i farvevalget.</span><span class="sxs-lookup"><span data-stu-id="c15d9-115">Select a color from the color selection.</span></span>
    * <span data-ttu-id="c15d9-116">Farverne bruges til at fremhæve job på listesiden for kanban-tidsplanen eller kanban-procesområdet.</span><span class="sxs-lookup"><span data-stu-id="c15d9-116">The colors are used to highlight the jobs on the kanban schedule list page or the kanban process board.</span></span>  
5. <span data-ttu-id="c15d9-117">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="c15d9-117">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="c15d9-118">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="c15d9-118">In the list, click the link in the selected row.</span></span>

## <a name="associate-product"></a><span data-ttu-id="c15d9-119">Tilknytte produkt</span><span class="sxs-lookup"><span data-stu-id="c15d9-119">Associate product</span></span>
1. <span data-ttu-id="c15d9-120">Tilknytte et bestemt produkt</span><span class="sxs-lookup"><span data-stu-id="c15d9-120">Associate a specific product</span></span>
    * <span data-ttu-id="c15d9-121">Der er to måder at knytte produkter til lean planlægningsgrupper: enten som et bestemt produkt (varerelationstype = vare) eller som en del af en varefordelingsnøgle (varerelationstype = gruppe).</span><span class="sxs-lookup"><span data-stu-id="c15d9-121">There are two ways to associate products to lean schedule groups, either as a specific product (Item relation type = Item) or as part of an item allocation key (item relation type = group).</span></span>    
2. <span data-ttu-id="c15d9-122">Vælg Vare i feltet Varerelationstype</span><span class="sxs-lookup"><span data-stu-id="c15d9-122">In the Item relation type field, select Item</span></span>
3. <span data-ttu-id="c15d9-123">Indtast en værdi i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="c15d9-123">In the Item number field, type a value.</span></span>
4. <span data-ttu-id="c15d9-124">Angiv et tal i feltet Gennemløbsforhold.</span><span class="sxs-lookup"><span data-stu-id="c15d9-124">In the Throughput ratio field, enter a number.</span></span>
    * <span data-ttu-id="c15d9-125">Standardgennemløbsforholdet er 1, hvilket betyder, at de relaterede produkter forbruger nøjagtigt den kapacitet, der er angivet i procesaktiviteterne for produktionsflowene.</span><span class="sxs-lookup"><span data-stu-id="c15d9-125">The default Throughput ratio is 1, which means that the related products consume exactly the capacity specified in the process activites of the production flows.</span></span> <span data-ttu-id="c15d9-126">Gennemløbsforhold > 1 definerer et højere ressourceforbrug, Gennemløbsforhold < 1 definerer et lavere ressourceforbrug.</span><span class="sxs-lookup"><span data-stu-id="c15d9-126">Throughput ratio > 1 defines a higher resource consumption, Throughput ratio < 1 defines a lower resource consumption.</span></span> <span data-ttu-id="c15d9-127">Forholdet bruges i omkostningsberegningen og i beregningen af kanban-jobforbruget.</span><span class="sxs-lookup"><span data-stu-id="c15d9-127">The ratio is used in the cost calculation and in the calculation of the kanban job consumption.</span></span>  

## <a name="associate-item-allocation-key"></a><span data-ttu-id="c15d9-128">Tilknytte varefordelingsnøgle</span><span class="sxs-lookup"><span data-stu-id="c15d9-128">Associate item allocation key</span></span>
1. <span data-ttu-id="c15d9-129">Tilknytte en varefordelingsnøgle</span><span class="sxs-lookup"><span data-stu-id="c15d9-129">Associate an item allocation key</span></span>
    * <span data-ttu-id="c15d9-130">Føj en tilknytning til en varefordelingsnøgle ved hjælp af varerelationstypen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="c15d9-130">Add an association to an item allocation key by using the Item relation type Group.</span></span>   <span data-ttu-id="c15d9-131">Bemærk, at denne proces skal du en budgetvarefordelingsnøgle, der er defineret i dataene.</span><span class="sxs-lookup"><span data-stu-id="c15d9-131">Note that for this process, you need a forecast item alllocation key defined in your data.</span></span>  
2. <span data-ttu-id="c15d9-132">Vælg Gruppe i feltet Varerelationstype</span><span class="sxs-lookup"><span data-stu-id="c15d9-132">In the Item relation type field, select Group</span></span>
3. <span data-ttu-id="c15d9-133">Klik på rullelisten i feltet Varefordelingsnøgle for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="c15d9-133">In the Item allocation key field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="c15d9-134">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="c15d9-134">In the list, click the link in the selected row.</span></span>

