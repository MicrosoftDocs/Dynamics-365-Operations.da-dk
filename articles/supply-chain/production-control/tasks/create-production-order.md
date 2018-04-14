---
title: Oprette en produktionsordre
description: Denne procedure viser, hvordan du opretter en produktionsordre.
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 0c83c8e4506db41a69e94f35272bb651197f3478
ms.contentlocale: da-dk
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-production-order"></a><span data-ttu-id="70683-103">Oprette en produktionsordre</span><span class="sxs-lookup"><span data-stu-id="70683-103">Create a production order</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="70683-104">Denne procedure viser, hvordan du opretter en produktionsordre.</span><span class="sxs-lookup"><span data-stu-id="70683-104">This procedure shows how to create a production order.</span></span> <span data-ttu-id="70683-105">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="70683-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="70683-106">Dette er den første procedure ud af syv, der beskriver produktionsordrens livscyklus.</span><span class="sxs-lookup"><span data-stu-id="70683-106">This is the first procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="create-a-production-order"></a><span data-ttu-id="70683-107">Oprette en produktionsordre</span><span class="sxs-lookup"><span data-stu-id="70683-107">Create a production order</span></span>
1. <span data-ttu-id="70683-108">Gå til Produktionsstyring > Produktionsordrer > Alle produktionsordrer.</span><span class="sxs-lookup"><span data-stu-id="70683-108">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="70683-109">Klik på Ny produktionsordre.</span><span class="sxs-lookup"><span data-stu-id="70683-109">Click New production order.</span></span>
3. <span data-ttu-id="70683-110">Skriv 'D0001' i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="70683-110">In the Item number field, type 'D0001'.</span></span>
4. <span data-ttu-id="70683-111">Angiv en dato i feltet Levering.</span><span class="sxs-lookup"><span data-stu-id="70683-111">In the Delivery field, enter a date.</span></span>
    * <span data-ttu-id="70683-112">Leveringsdatoen angiver, hvornår produktionsordren skal slutte med henblik på at levere til tiden.</span><span class="sxs-lookup"><span data-stu-id="70683-112">The delivery date indicates when the production order should end in order to deliver on time.</span></span> <span data-ttu-id="70683-113">Denne dato kan bruges i planlægningsprocessen.</span><span class="sxs-lookup"><span data-stu-id="70683-113">This date can be used in the scheduling process.</span></span> <span data-ttu-id="70683-114">Du kan f.eks. planlægge ordren bagud i forhold til leveringsdatoen.</span><span class="sxs-lookup"><span data-stu-id="70683-114">For example, you can schedule the order backward from the delivery date.</span></span>  
5. <span data-ttu-id="70683-115">Angiv antallet til '20'.</span><span class="sxs-lookup"><span data-stu-id="70683-115">Set Quantity to '20'.</span></span>
    * <span data-ttu-id="70683-116">Bemærk! Feltet Styklistenummer viser automatisk antallet i en aktiv stykliste for den aktuelle vare, men du kan ændre styklisten for produktionsordren ved at vælge en aktiv stykliste på listen over godkendte styklisteversioner.</span><span class="sxs-lookup"><span data-stu-id="70683-116">Note: The BOM number field automatically displays the number of any active BOM for the current item, but you can change the BOM for the production order by selecting an active BOM from the list of approved BOM versions.</span></span>    <span data-ttu-id="70683-117">Feltet Rutenummer viser automatisk antallet i en aktiv rute for den aktuelle vare, men du kan ændre ruten for produktionsordren ved at vælge en aktiv rute på listen over godkendte ruteversioner.</span><span class="sxs-lookup"><span data-stu-id="70683-117">The Route number field automatically displays the number of any active Route for the current item, but you can change the Route for the production order by selecting an active Route from the list of approved Route versions.</span></span>  
6. <span data-ttu-id="70683-118">Klik på Opret.</span><span class="sxs-lookup"><span data-stu-id="70683-118">Click Create.</span></span>

## <a name="validate-the-production-order"></a><span data-ttu-id="70683-119">Valider produktionsordren</span><span class="sxs-lookup"><span data-stu-id="70683-119">Validate the production order</span></span>
1. <span data-ttu-id="70683-120">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="70683-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="70683-121">Klik på linket til det produktionsordrenummer, du lige har oprettet.</span><span class="sxs-lookup"><span data-stu-id="70683-121">Click the link for the production order number that you have just created.</span></span> <span data-ttu-id="70683-122">Derved åbnes detaljesiden for ordren.</span><span class="sxs-lookup"><span data-stu-id="70683-122">This will open the details page for the order.</span></span>  
2. <span data-ttu-id="70683-123">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="70683-123">Click Edit.</span></span>
3. <span data-ttu-id="70683-124">Angiv en dato i feltet Levering.</span><span class="sxs-lookup"><span data-stu-id="70683-124">In the Delivery field, enter a date.</span></span>
    * <span data-ttu-id="70683-125">Du kan f.eks. ændre leveringsdatoen for produktionsordren.</span><span class="sxs-lookup"><span data-stu-id="70683-125">For example, you can change the delivery date for the production order.</span></span>  
4. <span data-ttu-id="70683-126">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="70683-126">Click Save.</span></span>
5. <span data-ttu-id="70683-127">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="70683-127">Close the page.</span></span>

## <a name="update-the-bom"></a><span data-ttu-id="70683-128">Opdater styklisten</span><span class="sxs-lookup"><span data-stu-id="70683-128">Update the BOM</span></span>
1. <span data-ttu-id="70683-129">Klik på Produktionsordre i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="70683-129">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="70683-130">Klik på Stykliste.</span><span class="sxs-lookup"><span data-stu-id="70683-130">Click BOM.</span></span>
    * <span data-ttu-id="70683-131">Åbn styklistesiden for at validere de styklistedata, der er kopieret fra standarddataene, da produktionsordren blev oprettet.</span><span class="sxs-lookup"><span data-stu-id="70683-131">Open the BOM page to validate the BOM data that was copied from the default data when the production order was created.</span></span> <span data-ttu-id="70683-132">I denne procedure skal du opdatere antallet for en stykliste.</span><span class="sxs-lookup"><span data-stu-id="70683-132">In this procedure, you need to update the quantity for a BOM.</span></span>  
3. <span data-ttu-id="70683-133">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="70683-133">Click Edit.</span></span>
4. <span data-ttu-id="70683-134">Angiv et tal i feltet Antal.</span><span class="sxs-lookup"><span data-stu-id="70683-134">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="70683-135">Ændring af antallet på styklistelinjen påvirker forkalkulationen af materialeforbruget for produktionsordren.</span><span class="sxs-lookup"><span data-stu-id="70683-135">Changing the quantity on the BOM line affects the cost estimate of material consumption for the production order.</span></span>  
5. <span data-ttu-id="70683-136">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="70683-136">Click Save.</span></span>
6. <span data-ttu-id="70683-137">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="70683-137">Close the page.</span></span>

## <a name="update-the-production-route"></a><span data-ttu-id="70683-138">Opdater produktionsruten</span><span class="sxs-lookup"><span data-stu-id="70683-138">Update the production route</span></span>
1. <span data-ttu-id="70683-139">Klik på Produktionsordre i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="70683-139">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="70683-140">Klik på Rute.</span><span class="sxs-lookup"><span data-stu-id="70683-140">Click Route.</span></span>
    * <span data-ttu-id="70683-141">Åbn rutesiden for at validere dataene i den produktionsrute, der er kopieret fra standarddataene, da ordren blev oprettet.</span><span class="sxs-lookup"><span data-stu-id="70683-141">Open the Route page to validate the data of the production route that was copied from the default data when the order was created.</span></span> <span data-ttu-id="70683-142">I denne procedure skal du opdatere antallet for en af operationerne i produktionsruten.</span><span class="sxs-lookup"><span data-stu-id="70683-142">In this procedure, you need to update the quantity for one of the operations in the production route.</span></span>  
3. <span data-ttu-id="70683-143">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="70683-143">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="70683-144">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="70683-144">Click Edit.</span></span>
5. <span data-ttu-id="70683-145">I feltet Procesantal skal du angive et tal.</span><span class="sxs-lookup"><span data-stu-id="70683-145">In the Process qty. field, enter a number.</span></span>
    * <span data-ttu-id="70683-146">Ændring af procestiden påvirker det beregnede ruteforbrug og omkostninger for produktionsordren.</span><span class="sxs-lookup"><span data-stu-id="70683-146">Changing the process time affects the estimated route consumption and the cost of the production order.</span></span>  
6. <span data-ttu-id="70683-147">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="70683-147">Click Save.</span></span>
7. <span data-ttu-id="70683-148">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="70683-148">Close the page.</span></span>

