--- 
title: Oprette en materialeplan for samprodukter
description: "Produktionsplanlæggeren planlægger materialebehovet for varer, der er formelsamprodukter."
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: adc1e520ce9ec705555939f29008d7fc4494999a
ms.contentlocale: da-dk
ms.lasthandoff: 08/07/2018

---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="3ee7d-103">Oprette en materialeplan for samprodukter</span><span class="sxs-lookup"><span data-stu-id="3ee7d-103">Create a material plan for co-products</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3ee7d-104">Produktionsplanlæggeren planlægger materialebehovet for varer, der er formelsamprodukter.</span><span class="sxs-lookup"><span data-stu-id="3ee7d-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="3ee7d-105">Det demodatafirma, der bruges til at oprette denne procedure, er USP2.</span><span class="sxs-lookup"><span data-stu-id="3ee7d-105">The demo data company used to create this procedure is USP2.</span></span>


## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="3ee7d-106">Opret krav om et samprodukt</span><span class="sxs-lookup"><span data-stu-id="3ee7d-106">Create requirement for a co-product</span></span>
1. <span data-ttu-id="3ee7d-107">Gå til Standarddashboard.</span><span class="sxs-lookup"><span data-stu-id="3ee7d-107">Go to Default dashboard.</span></span>
2. <span data-ttu-id="3ee7d-108">Klik på Salgsordrebehandling og -forespørgsel.</span><span class="sxs-lookup"><span data-stu-id="3ee7d-108">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="3ee7d-109">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="3ee7d-109">Click New.</span></span>
4. <span data-ttu-id="3ee7d-110">Klik på Salgsordre.</span><span class="sxs-lookup"><span data-stu-id="3ee7d-110">Click Sales order.</span></span>
5. <span data-ttu-id="3ee7d-111">Skriv en værdi i feltet Kundekonto.</span><span class="sxs-lookup"><span data-stu-id="3ee7d-111">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="3ee7d-112">Eksempel: US-001</span><span class="sxs-lookup"><span data-stu-id="3ee7d-112">Example: US-001</span></span>  
6. <span data-ttu-id="3ee7d-113">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="3ee7d-113">Click OK.</span></span>
7. <span data-ttu-id="3ee7d-114">Indtast en værdi i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="3ee7d-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="3ee7d-115">Eksempel: P6003</span><span class="sxs-lookup"><span data-stu-id="3ee7d-115">Example: P6003</span></span>  
8. <span data-ttu-id="3ee7d-116">Angiv et tal i feltet Antal.</span><span class="sxs-lookup"><span data-stu-id="3ee7d-116">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="3ee7d-117">Eksempel: 50000</span><span class="sxs-lookup"><span data-stu-id="3ee7d-117">Example: 50000</span></span>  
9. <span data-ttu-id="3ee7d-118">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="3ee7d-118">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="3ee7d-119">Oprette en materialeplan for samprodukter</span><span class="sxs-lookup"><span data-stu-id="3ee7d-119">Create a material plan for co-products</span></span>
1. <span data-ttu-id="3ee7d-120">Klik på Varedisponering.</span><span class="sxs-lookup"><span data-stu-id="3ee7d-120">Click Master planning.</span></span>
2. <span data-ttu-id="3ee7d-121">Klik på rullelisten i feltet Plan for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="3ee7d-121">In the Plan field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="3ee7d-122">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="3ee7d-122">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="3ee7d-123">Eksempel: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="3ee7d-123">Example: MasterPlan</span></span>  
4. <span data-ttu-id="3ee7d-124">Klik på Kør.</span><span class="sxs-lookup"><span data-stu-id="3ee7d-124">Click Run.</span></span>
5. <span data-ttu-id="3ee7d-125">Udvis eller skjul sektionen Poster, der skal indgå.</span><span class="sxs-lookup"><span data-stu-id="3ee7d-125">Expand or collapse the Records to include section.</span></span>
6. <span data-ttu-id="3ee7d-126">Klik på Filtrér.</span><span class="sxs-lookup"><span data-stu-id="3ee7d-126">Click Filter.</span></span>
7. <span data-ttu-id="3ee7d-127">Vælg rækken for Felt = Varenummer på listen.</span><span class="sxs-lookup"><span data-stu-id="3ee7d-127">In the list, select the row for Field = Item number.</span></span>
8. <span data-ttu-id="3ee7d-128">Skriv en værdi i feltet Kriterier.</span><span class="sxs-lookup"><span data-stu-id="3ee7d-128">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="3ee7d-129">Eksempel: P6003</span><span class="sxs-lookup"><span data-stu-id="3ee7d-129">Example: P6003</span></span>  
9. <span data-ttu-id="3ee7d-130">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="3ee7d-130">Click OK.</span></span>
10. <span data-ttu-id="3ee7d-131">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="3ee7d-131">Click OK.</span></span>
11. <span data-ttu-id="3ee7d-132">Klik på Ordreforslag.</span><span class="sxs-lookup"><span data-stu-id="3ee7d-132">Click Planned orders.</span></span>
12. <span data-ttu-id="3ee7d-133">Brug Quick Filter til at finde poster.</span><span class="sxs-lookup"><span data-stu-id="3ee7d-133">Use the Quick Filter to find records.</span></span> <span data-ttu-id="3ee7d-134">Filtrer f.eks. efter feltet Varenummer med værdien "P6000".</span><span class="sxs-lookup"><span data-stu-id="3ee7d-134">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="3ee7d-135">Filtrer efter den formelvare, der har et samprodukt af den vare, du har oprettet en salgsordre for.</span><span class="sxs-lookup"><span data-stu-id="3ee7d-135">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
13. <span data-ttu-id="3ee7d-136">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="3ee7d-136">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="3ee7d-137">Vælg en af de rækker, der returneres af filteret.</span><span class="sxs-lookup"><span data-stu-id="3ee7d-137">Select any of the rows returned by the filter.</span></span>  
14. <span data-ttu-id="3ee7d-138">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="3ee7d-138">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="3ee7d-139">Udvid eller skjul sektionen Udligning.</span><span class="sxs-lookup"><span data-stu-id="3ee7d-139">Expand or collapse the Pegging section.</span></span>
16. <span data-ttu-id="3ee7d-140">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="3ee7d-140">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="3ee7d-141">Ordreforslaget er udlignet til salgsordren for samproduktet.</span><span class="sxs-lookup"><span data-stu-id="3ee7d-141">The planned order is pegged to the sales order for the co-product.</span></span>  
17. <span data-ttu-id="3ee7d-142">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="3ee7d-142">Close the page.</span></span>


