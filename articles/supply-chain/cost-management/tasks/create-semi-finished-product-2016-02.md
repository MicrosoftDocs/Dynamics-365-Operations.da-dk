---
title: Oprette et halvfærdigt produkt (kun februar 2016)
description: Denne opgave drejer sig om oprettelse af et halvfabrikataprodukt.
author: ShylaThompson
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 76fcba3732879f85c9bf0faa6d2481b9c5313a17
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1563175"
---
# <a name="create-a-semi-finished-product-february-2016-only"></a><span data-ttu-id="c405c-103">Oprette et halvfærdigt produkt (kun februar 2016)</span><span class="sxs-lookup"><span data-stu-id="c405c-103">Create a semi-finished product (February 2016 only)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c405c-104">Denne opgave drejer sig om oprettelse af et halvfabrikataprodukt.</span><span class="sxs-lookup"><span data-stu-id="c405c-104">This task focuses on creating a semi-finished product.</span></span> <span data-ttu-id="c405c-105">Det er den anden opgave i styklisteberegningsserien.</span><span class="sxs-lookup"><span data-stu-id="c405c-105">It is the second task in the BOM calculation series.</span></span> <span data-ttu-id="c405c-106">Det demodatafirma, der bruges til at oprette denne opgave, er USMF.</span><span class="sxs-lookup"><span data-stu-id="c405c-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="c405c-107">Gå til Administration af produktoplysninger > Produkter > Frigivne produkter.</span><span class="sxs-lookup"><span data-stu-id="c405c-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="c405c-108">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="c405c-108">Click New.</span></span>
3. <span data-ttu-id="c405c-109">Skriv en værdi i feltet Produktnummer.</span><span class="sxs-lookup"><span data-stu-id="c405c-109">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="c405c-110">I dette eksempel skal du skrive BOM_2.</span><span class="sxs-lookup"><span data-stu-id="c405c-110">For this example, type BOM_2.</span></span>  
4. <span data-ttu-id="c405c-111">Indtast eller vælg en værdi i feltet Varemodelgruppe.</span><span class="sxs-lookup"><span data-stu-id="c405c-111">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="c405c-112">Vælg STD.</span><span class="sxs-lookup"><span data-stu-id="c405c-112">Select STD.</span></span> <span data-ttu-id="c405c-113">STD står for standardomkostninger og er den mest almindeligt anvendte model, når du arbejder med omkostningsberegninger.</span><span class="sxs-lookup"><span data-stu-id="c405c-113">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="c405c-114">Indtast eller vælg en værdi i feltet Varegruppe.</span><span class="sxs-lookup"><span data-stu-id="c405c-114">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="c405c-115">Vælg f.eks. Lyd.</span><span class="sxs-lookup"><span data-stu-id="c405c-115">For example, select Audio.</span></span> <span data-ttu-id="c405c-116">Dette har ingen indflydelse på omkostningsberegninger.</span><span class="sxs-lookup"><span data-stu-id="c405c-116">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="c405c-117">Indtast eller vælg en værdi i feltet Lagringsdimensionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="c405c-117">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="c405c-118">Vælg SiteWH.</span><span class="sxs-lookup"><span data-stu-id="c405c-118">Select SiteWH.</span></span> <span data-ttu-id="c405c-119">Kun lokalitet og lagersted bruges til dette eksempel.</span><span class="sxs-lookup"><span data-stu-id="c405c-119">Only Site and Warehouse will be used for this example.</span></span>  
7. <span data-ttu-id="c405c-120">Indtast eller vælg en værdi i feltet Sporingsdimensionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="c405c-120">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="c405c-121">Sporingsdimensioner bliver ikke brugt i dette eksempel. Vælg Ingen.</span><span class="sxs-lookup"><span data-stu-id="c405c-121">Tracking dimensions will not be used for this example, select None.</span></span>  
8. <span data-ttu-id="c405c-122">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="c405c-122">Click OK.</span></span>
9. <span data-ttu-id="c405c-123">Klik på Styr lager i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="c405c-123">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="c405c-124">Klik på Standardindstillinger for ordre.</span><span class="sxs-lookup"><span data-stu-id="c405c-124">Click Default order settings.</span></span>
11. <span data-ttu-id="c405c-125">Vælg en indstilling i feltet Produktion.</span><span class="sxs-lookup"><span data-stu-id="c405c-125">In the Default order type field, select 'Production'.</span></span>
    * <span data-ttu-id="c405c-126">Da dette er et halvfabrikataprodukt, der skal produceres, skal du vælge Produktion.</span><span class="sxs-lookup"><span data-stu-id="c405c-126">Because this is a semi-finished product that will be produced, select Production.</span></span>  
12. <span data-ttu-id="c405c-127">Indtast eller vælg en værdi i feltet Købssted.</span><span class="sxs-lookup"><span data-stu-id="c405c-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="c405c-128">I dette eksempel skal du vælge Sted 1.</span><span class="sxs-lookup"><span data-stu-id="c405c-128">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="c405c-129">Indtast eller vælg en værdi i feltet Sted for lager.</span><span class="sxs-lookup"><span data-stu-id="c405c-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="c405c-130">I dette eksempel skal du vælge Sted 1.</span><span class="sxs-lookup"><span data-stu-id="c405c-130">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="c405c-131">Indtast eller vælg en værdi i feltet Salgssted.</span><span class="sxs-lookup"><span data-stu-id="c405c-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="c405c-132">I dette eksempel skal du vælge Sted 1.</span><span class="sxs-lookup"><span data-stu-id="c405c-132">For this example, select Site 1.</span></span>  
15. <span data-ttu-id="c405c-133">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="c405c-133">Close the page.</span></span>
16. <span data-ttu-id="c405c-134">Klik på Administrer omkostninger i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="c405c-134">On the Action Pane, click Manage costs.</span></span>
17. <span data-ttu-id="c405c-135">Klik på Varepris.</span><span class="sxs-lookup"><span data-stu-id="c405c-135">Click Item price.</span></span>
18. <span data-ttu-id="c405c-136">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="c405c-136">Click New.</span></span>
19. <span data-ttu-id="c405c-137">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="c405c-137">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="c405c-138">Indtast eller vælg en værdi i feltet Version.</span><span class="sxs-lookup"><span data-stu-id="c405c-138">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="c405c-139">I dette eksempel skal du vælge Version 10.</span><span class="sxs-lookup"><span data-stu-id="c405c-139">For this example, select Version 10.</span></span>  
21. <span data-ttu-id="c405c-140">Indtast eller vælg en værdi i feltet Lokation.</span><span class="sxs-lookup"><span data-stu-id="c405c-140">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="c405c-141">I dette eksempel skal du vælge Sted 1.</span><span class="sxs-lookup"><span data-stu-id="c405c-141">For this example, select Site 1.</span></span>  
22. <span data-ttu-id="c405c-142">Angiv Pris til "10".</span><span class="sxs-lookup"><span data-stu-id="c405c-142">Set Price to '10'.</span></span>
    * <span data-ttu-id="c405c-143">I dette eksempel skal du skrive en kostpris på 10.</span><span class="sxs-lookup"><span data-stu-id="c405c-143">For this example, type a cost price of 10.</span></span>  
23. <span data-ttu-id="c405c-144">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="c405c-144">Click Save.</span></span>
24. <span data-ttu-id="c405c-145">Klik på Aktivér afventende pris(er).</span><span class="sxs-lookup"><span data-stu-id="c405c-145">Click Activate pending price(s).</span></span>
25. <span data-ttu-id="c405c-146">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="c405c-146">Close the page.</span></span>
26. <span data-ttu-id="c405c-147">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="c405c-147">Close the page.</span></span>
27. <span data-ttu-id="c405c-148">Klik på BOM_2 for at åbne den.</span><span class="sxs-lookup"><span data-stu-id="c405c-148">Click BOM_2 to open it.</span></span>
28. <span data-ttu-id="c405c-149">Udvid sektionen Administrer omkostninger.</span><span class="sxs-lookup"><span data-stu-id="c405c-149">Expand the Manage costs section.</span></span>
29. <span data-ttu-id="c405c-150">Indtast eller vælg en værdi i feltet Omkostningsgruppe.</span><span class="sxs-lookup"><span data-stu-id="c405c-150">In the Cost group field, enter or select a value.</span></span>
    * <span data-ttu-id="c405c-151">Vælg Omkostningsgruppe M1 i dette eksempel.</span><span class="sxs-lookup"><span data-stu-id="c405c-151">For this example, select Cost group M1.</span></span>  
30. <span data-ttu-id="c405c-152">Brug genvejen til lagring af en post.</span><span class="sxs-lookup"><span data-stu-id="c405c-152">Use the shortcut for saving a record.</span></span>
31. <span data-ttu-id="c405c-153">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="c405c-153">Close the page.</span></span>

