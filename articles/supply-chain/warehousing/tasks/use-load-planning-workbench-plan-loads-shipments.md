---
title: Planlægge laster og forsendelser ved hjælp af lastplanlægningspanelet
description: Dette emne beskriver, hvordan lastplanlægningspanelet bruges til at oprette en belastning for en salgsordre.
author: ShylaThompson
manager: AnnBe
ms.date: 07/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8a51031647e270662f37138848b0db9ed08d544e
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145870"
---
# <a name="plan-loads-and-shipments-using-the-load-planning-workbench"></a><span data-ttu-id="8df48-103">Planlægge laster og forsendelser ved hjælp af lastplanlægningspanelet</span><span class="sxs-lookup"><span data-stu-id="8df48-103">Plan loads and shipments using the Load planning workbench</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8df48-104">Dette emne beskriver, hvordan lastplanlægningspanelet bruges til at oprette en belastning for en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="8df48-104">This topic shows how to use the load planning workbench to create a load for a sales order.</span></span> <span data-ttu-id="8df48-105">Som en forudsætning skal vi skal oprette salgsordren.</span><span class="sxs-lookup"><span data-stu-id="8df48-105">As a prerequisite we'll create the sales order first.</span></span> <span data-ttu-id="8df48-106">Denne procedure er en del af det daglige arbejde for transportkoordinatoren.</span><span class="sxs-lookup"><span data-stu-id="8df48-106">This procedure is part of the daily work for the transportation coordinator.</span></span> <span data-ttu-id="8df48-107">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="8df48-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-sales-order"></a><span data-ttu-id="8df48-108">Oprette en salgsordre</span><span class="sxs-lookup"><span data-stu-id="8df48-108">Create a sales order</span></span>
1. <span data-ttu-id="8df48-109">Gå til **Navigationsrude > Moduler > Debitor > Ordrer > Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="8df48-109">Go to the **Navigation pane > Modules > Accounts receivable > Orders > All sales orders**.</span></span>
2. <span data-ttu-id="8df48-110">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="8df48-110">Select **New**.</span></span>
3. <span data-ttu-id="8df48-111">Vælg rullelisten i feltet **Kundekonto** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="8df48-111">In the **Customer account** field, select the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="8df48-112">Vælg konto **US-004**.</span><span class="sxs-lookup"><span data-stu-id="8df48-112">Select account **US-004**.</span></span>
5. <span data-ttu-id="8df48-113">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="8df48-113">Select **OK**.</span></span>
6. <span data-ttu-id="8df48-114">Klik på rullelisten i feltet **Varenummer** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="8df48-114">In the **Item number** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="8df48-115">Vælg vare **A0001**.</span><span class="sxs-lookup"><span data-stu-id="8df48-115">Select item **A0001**.</span></span> <span data-ttu-id="8df48-116">**A0001** er aktiveret for transportstyring.</span><span class="sxs-lookup"><span data-stu-id="8df48-116">**A0001** is enabled for transportation management.</span></span>  
8. <span data-ttu-id="8df48-117">Klik på rullelisten i feltet **Sted** for at åbne opslaget, og vælg derefter en vare.</span><span class="sxs-lookup"><span data-stu-id="8df48-117">In the **Site** field, select the drop-down button to open the lookup, then select an item.</span></span>
9. <span data-ttu-id="8df48-118">Angiv et tal i feltet **Antal**.</span><span class="sxs-lookup"><span data-stu-id="8df48-118">In the **Quantity** field, enter a number.</span></span>
10. <span data-ttu-id="8df48-119">Skriv i dette eksempel "24" i feltet **Lagerlokation**.</span><span class="sxs-lookup"><span data-stu-id="8df48-119">In the **Warehouse** field, type '24' for this example.</span></span> <span data-ttu-id="8df48-120">Dette lagersted er aktiveret for transportstyring og avanceret lagerstedsstyring.</span><span class="sxs-lookup"><span data-stu-id="8df48-120">This warehouse is enabled for transportation management and advanced warehouse management.</span></span>  
11. <span data-ttu-id="8df48-121">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="8df48-121">Select **Save**.</span></span>
12. <span data-ttu-id="8df48-122">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="8df48-122">Close the page.</span></span>

## <a name="create-a-new-load"></a><span data-ttu-id="8df48-123">Opret en ny belastning</span><span class="sxs-lookup"><span data-stu-id="8df48-123">Create a new load</span></span>
1. <span data-ttu-id="8df48-124">Gå til **Navigationsrude > Moduler > Transportstyring > Planlægning > lastplanlægningspanelet**.</span><span class="sxs-lookup"><span data-stu-id="8df48-124">Go to the **Navigation pane > Modules > Transportation management > Planning > Load planning workbench**.</span></span>
2. <span data-ttu-id="8df48-125">Vælg fanen **Salgslinjer**. Nu kan du opbygge belastningen for den salgsordre, som du lige har oprettet.</span><span class="sxs-lookup"><span data-stu-id="8df48-125">Select the **Sales lines** tab. Now you'll build the load for the sales order that you just created.</span></span> <span data-ttu-id="8df48-126">Belastninger kan bygges baseret på udbud og efterspørgsel fra købsordrer, flytteordrer og salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="8df48-126">Loads can be built based on supply and demand from purchase orders, transfer orders, and sales orders.</span></span>  
3. <span data-ttu-id="8df48-127">Klik på fanen **Udbud og efterspørgsel** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="8df48-127">On the Action Pane, select **Supply and demand**.</span></span>
4. <span data-ttu-id="8df48-128">Vælg **Til ny last**.</span><span class="sxs-lookup"><span data-stu-id="8df48-128">Select **To new load**.</span></span>
5. <span data-ttu-id="8df48-129">Vælg feltet **Lastskabelons-Id** i rullelisten for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="8df48-129">In the **Load template ID** field, select the drop-down button to open the lookup.</span></span> <span data-ttu-id="8df48-130">Lastskabelonen definerer det maksimale mål for vægt og volumen af den samlede belastning.</span><span class="sxs-lookup"><span data-stu-id="8df48-130">The Load template defines maximum measurements for weight and volume of the entire load.</span></span> <span data-ttu-id="8df48-131">For eksempel kan lastskabelonen repræsentere størrelsen af en container eller lastbil.</span><span class="sxs-lookup"><span data-stu-id="8df48-131">For example, the load template might represent the size of a container or truck.</span></span> <span data-ttu-id="8df48-132">Vælg en vare.</span><span class="sxs-lookup"><span data-stu-id="8df48-132">Select an item.</span></span>
6. <span data-ttu-id="8df48-133">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="8df48-133">Select **OK**.</span></span>

## <a name="rate-and-route-the-load"></a><span data-ttu-id="8df48-134">Vurder og ruteplanlæg belastningen</span><span class="sxs-lookup"><span data-stu-id="8df48-134">Rate and route the load</span></span>
1. <span data-ttu-id="8df48-135">Vælg **Bedømmelse og ruteplanlægning**.</span><span class="sxs-lookup"><span data-stu-id="8df48-135">Select **Rating and routing**.</span></span>
2. <span data-ttu-id="8df48-136">Vælg **Panelet bedøm rute**.</span><span class="sxs-lookup"><span data-stu-id="8df48-136">Select **Rate route workbench**.</span></span>
3. <span data-ttu-id="8df48-137">Vælg **Bedøm butik**.</span><span class="sxs-lookup"><span data-stu-id="8df48-137">Select **Rate shop**.</span></span>
4. <span data-ttu-id="8df48-138">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="8df48-138">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="8df48-139">Vælg **Tildel**.</span><span class="sxs-lookup"><span data-stu-id="8df48-139">Select **Assign**.</span></span>
6. <span data-ttu-id="8df48-140">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="8df48-140">Close the page.</span></span>

