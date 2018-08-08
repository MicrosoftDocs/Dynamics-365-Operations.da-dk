--- 
title: "Arrangere produktionsjob i forløb til procesproduktion"
description: "Denne procedure bruger malingsprodukter som et eksempel til at vise, hvordan du sorterer ordreforslag i overensstemmelse med prioriteten af farve og pakkestørrelse."
author: ChristianRytt
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
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 24fc5b62bac6d025c435090c030276e416cd424c
ms.contentlocale: da-dk
ms.lasthandoff: 08/07/2018

---
# <a name="sequence-production-jobs-for-process-manufacturing"></a><span data-ttu-id="15c97-103">Arrangere produktionsjob i forløb til procesproduktion</span><span class="sxs-lookup"><span data-stu-id="15c97-103">Sequence production jobs for process manufacturing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="15c97-104">Denne procedure bruger malingsprodukter som et eksempel til at vise, hvordan du sorterer ordreforslag i overensstemmelse med prioriteten af farve og pakkestørrelse.</span><span class="sxs-lookup"><span data-stu-id="15c97-104">This procedure uses paint products as an example to show how to sequence planned orders according to the priority of color and package size.</span></span> <span data-ttu-id="15c97-105">Det demodatafirma, der bruges til at oprette denne procedure, er USPI.</span><span class="sxs-lookup"><span data-stu-id="15c97-105">The demo data company used to create this procedure is USPI.</span></span> <span data-ttu-id="15c97-106">Denne procedure er beregnet til produktionsplanlæggeren.</span><span class="sxs-lookup"><span data-stu-id="15c97-106">This procedure is intended for the production planner.</span></span>


## <a name="run-master-planning-for-uspi"></a><span data-ttu-id="15c97-107">Køre varedisponering for USPI</span><span class="sxs-lookup"><span data-stu-id="15c97-107">Run master planning for USPI</span></span>
1. <span data-ttu-id="15c97-108">Gå til Varedisponering > Varedisponering > Kørsel > Varedisponering.</span><span class="sxs-lookup"><span data-stu-id="15c97-108">Go to Master planning > Master planning > Run > Master planning.</span></span>
2. <span data-ttu-id="15c97-109">Klik på rullelisten i feltet Behovsplan for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="15c97-109">In the Master plan field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="15c97-110">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="15c97-110">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="15c97-111">Vælg MasterPlan.</span><span class="sxs-lookup"><span data-stu-id="15c97-111">Select MasterPlan.</span></span>  
4. <span data-ttu-id="15c97-112">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="15c97-112">Click OK.</span></span>
    * <span data-ttu-id="15c97-113">Dermed startes Varedisponering, herunder afviklingsrækkefølgen.</span><span class="sxs-lookup"><span data-stu-id="15c97-113">This starts Master Planning, including the sequence process.</span></span> <span data-ttu-id="15c97-114">Denne proces kan tage nogle få minutter.</span><span class="sxs-lookup"><span data-stu-id="15c97-114">This process can take a few minutes.</span></span>  

## <a name="view-planned-orders-for-the-paint-products"></a><span data-ttu-id="15c97-115">Få vist ordreforslag for malingsprodukter</span><span class="sxs-lookup"><span data-stu-id="15c97-115">View planned orders for the paint products</span></span>
1. <span data-ttu-id="15c97-116">Gå til Varedisponering > Varedisponering > Ordreforslag.</span><span class="sxs-lookup"><span data-stu-id="15c97-116">Go to Master planning > Master planning > Planned orders.</span></span>
2. <span data-ttu-id="15c97-117">Udvid faktaboksen Vareoplysninger.</span><span class="sxs-lookup"><span data-stu-id="15c97-117">Expand the Item details FactBox.</span></span>
3. <span data-ttu-id="15c97-118">Udvid faktaboksen Planoplysninger.</span><span class="sxs-lookup"><span data-stu-id="15c97-118">Expand the Schedule details FactBox.</span></span>
4. <span data-ttu-id="15c97-119">Klik på rullelisten i feltet Plan for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="15c97-119">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="15c97-120">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="15c97-120">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="15c97-121">Vælg MasterPlan.</span><span class="sxs-lookup"><span data-stu-id="15c97-121">Select MasterPlan.</span></span>  
6. <span data-ttu-id="15c97-122">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="15c97-122">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="15c97-123">Brug Quick Filter til at filtrere på feltet Varenummer med værdien 'P300'.</span><span class="sxs-lookup"><span data-stu-id="15c97-123">Use the Quick Filter to filter on the Item number field with a value of 'P300'.</span></span>
    * <span data-ttu-id="15c97-124">Lås op for at rulle til højre for at få vist bestillingsdato og leveringsdato.</span><span class="sxs-lookup"><span data-stu-id="15c97-124">Unlock to scroll to the right to see the order date and delivery date.</span></span> <span data-ttu-id="15c97-125">Bemærk, at disse varer har en ordredato for I dag, og leveringsdatoerne for ordreforslagene er ikke sorteret efter prioritet for farve og pakkestørrelse, som vist i produktnavnet.</span><span class="sxs-lookup"><span data-stu-id="15c97-125">Notice that these items have an order date of Today and the delivery dates for the planned orders are not sequenced after the priority of color and package size, as shown in the product name.</span></span> <span data-ttu-id="15c97-126">Du kan placere markøren over et varenummer for at få vist produktets navn og prioritet.</span><span class="sxs-lookup"><span data-stu-id="15c97-126">You can hover over an item number to see the product name and priority.</span></span>  

## <a name="sequence-planned-orders-for-paint"></a><span data-ttu-id="15c97-127">Sortere ordreforslag for malingsprodukter</span><span class="sxs-lookup"><span data-stu-id="15c97-127">Sequence planned orders for paint</span></span>
1. <span data-ttu-id="15c97-128">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="15c97-128">Close the page.</span></span>
2. <span data-ttu-id="15c97-129">Gå til Varedisponering > Varedisponering > Sorterede ordreforslag.</span><span class="sxs-lookup"><span data-stu-id="15c97-129">Go to Master planning > Master planning > Sequenced planned orders.</span></span>
3. <span data-ttu-id="15c97-130">Udvid faktaboksen Vareoplysninger.</span><span class="sxs-lookup"><span data-stu-id="15c97-130">Expand the Item details FactBox.</span></span>
4. <span data-ttu-id="15c97-131">Udvid faktaboksen Planoplysninger.</span><span class="sxs-lookup"><span data-stu-id="15c97-131">Expand the Schedule details FactBox.</span></span>
    * <span data-ttu-id="15c97-132">Bemærk: Her kan du se, at Start dato/klokkeslæt for ordreforslagene sorteres efter farve og pakkestørrelse i et tidsgruppeperiode på 28 dage.</span><span class="sxs-lookup"><span data-stu-id="15c97-132">Note: Here you see that the Start date/time for the planned orders are sequenced according to color and package size within a bucket period of 28 days.</span></span> <span data-ttu-id="15c97-133">Disse perioder er defineret af et tal i feltet Kampagne.</span><span class="sxs-lookup"><span data-stu-id="15c97-133">These periods are defined by a number in the field Campaign.</span></span> <span data-ttu-id="15c97-134">Formlen for sortering af ordreforslag fungerer som den typiske formular for ordreforslag, og produktionsplanlæggeren kan autorisere ordreforslagene her.</span><span class="sxs-lookup"><span data-stu-id="15c97-134">The sequenced planned order form acts like the typical planned order form, and the production planner can firm the planned orders here.</span></span>  
5. <span data-ttu-id="15c97-135">Markér alle rækker.</span><span class="sxs-lookup"><span data-stu-id="15c97-135">Mark all rows.</span></span>
6. <span data-ttu-id="15c97-136">Klik på Acceptér.</span><span class="sxs-lookup"><span data-stu-id="15c97-136">Click Accept.</span></span>
    * <span data-ttu-id="15c97-137">Dette vil opdatere ordreforslagene med den valgte rækkefølge for håndtering ved hjælp af Udsæt eller Fremskynd.</span><span class="sxs-lookup"><span data-stu-id="15c97-137">This will update the planned orders with the selected sequence action of either Postpone or Advance.</span></span>  

## <a name="verify-the-sequence-of-the-planned-orders"></a><span data-ttu-id="15c97-138">Kontrollere rækkefølgen af ordreforslag</span><span class="sxs-lookup"><span data-stu-id="15c97-138">Verify the sequence of the planned orders</span></span>
1. <span data-ttu-id="15c97-139">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="15c97-139">Close the page.</span></span>
2. <span data-ttu-id="15c97-140">Gå til Varedisponering > Varedisponering > Ordreforslag.</span><span class="sxs-lookup"><span data-stu-id="15c97-140">Go to Master planning > Master planning > Planned orders.</span></span>
3. <span data-ttu-id="15c97-141">Udvid faktaboksen Vareoplysninger.</span><span class="sxs-lookup"><span data-stu-id="15c97-141">Expand the Item details FactBox.</span></span>
4. <span data-ttu-id="15c97-142">Udvid faktaboksen Planoplysninger.</span><span class="sxs-lookup"><span data-stu-id="15c97-142">Expand the Schedule details FactBox.</span></span>
5. <span data-ttu-id="15c97-143">Klik på rullelisten i feltet Plan for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="15c97-143">In the Plan field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="15c97-144">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="15c97-144">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="15c97-145">Vælg MasterPlan.</span><span class="sxs-lookup"><span data-stu-id="15c97-145">Select MasterPlan.</span></span>  
7. <span data-ttu-id="15c97-146">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="15c97-146">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="15c97-147">Brug Quick Filter til at filtrere på feltet Varenummer med værdien 'P300'.</span><span class="sxs-lookup"><span data-stu-id="15c97-147">Use the Quick Filter to filter on the Item number field with a value of 'P300'.</span></span>
    * <span data-ttu-id="15c97-148">Bemærk, at ordrerne nu sorteres efter prioritet for farve og størrelse, og ordreforslagene begynder på den tidligste ordredato og leveringsdato.</span><span class="sxs-lookup"><span data-stu-id="15c97-148">Notice that the orders now are sequenced according to the priority of color and size and the planned orders start at the earliest order date and delivery date.</span></span> <span data-ttu-id="15c97-149">Validere kolonnen Ordredato eller Startdato i faktaboksen Planoplysninger.</span><span class="sxs-lookup"><span data-stu-id="15c97-149">Validate the Order date column or the Start date in the Schedule details FactBox.</span></span>  


