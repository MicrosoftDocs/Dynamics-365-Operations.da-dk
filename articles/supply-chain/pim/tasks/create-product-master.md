--- 
title: Oprette en produktmaster
description: Opret en produktmaster for de foruddefinerede varianter.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 6e34f7c630e872468d888938e0f1aa57f3f0d4c4
ms.contentlocale: da-dk
ms.lasthandoff: 09/14/2018

---
# <a name="create-a-product-master"></a><span data-ttu-id="90438-103">Oprette en produktmaster</span><span class="sxs-lookup"><span data-stu-id="90438-103">Create a product master</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="90438-104">Opret en produktmaster for de foruddefinerede varianter.</span><span class="sxs-lookup"><span data-stu-id="90438-104">Create a product master for the predefined variants.</span></span> <span data-ttu-id="90438-105">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="90438-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="90438-106">Denne procedure er beregnet til produktdesigneren.</span><span class="sxs-lookup"><span data-stu-id="90438-106">This procedure is intended for the product designer.</span></span>


## <a name="create-a-new-product-master"></a><span data-ttu-id="90438-107">Opret en ny produktmaster</span><span class="sxs-lookup"><span data-stu-id="90438-107">Create a new product master</span></span>
1. <span data-ttu-id="90438-108">Gå til Administration af produktoplysninger > Produkter > Produktmastere.</span><span class="sxs-lookup"><span data-stu-id="90438-108">Go to Product information management > Products > Product masters.</span></span>
2. <span data-ttu-id="90438-109">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="90438-109">Click New.</span></span>
3. <span data-ttu-id="90438-110">Skriv en værdi i feltet Produktnummer.</span><span class="sxs-lookup"><span data-stu-id="90438-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="90438-111">Tallet skal være entydigt.</span><span class="sxs-lookup"><span data-stu-id="90438-111">The number must be unique.</span></span> <span data-ttu-id="90438-112">En nummerserie kan konfigureres for feltet Produktnummer.</span><span class="sxs-lookup"><span data-stu-id="90438-112">A number sequence can be set for the Product number field.</span></span> <span data-ttu-id="90438-113">I dette tilfælde skal brugeren ikke at angive en værdi.</span><span class="sxs-lookup"><span data-stu-id="90438-113">In this case, the user doesn't have to enter a value.</span></span>  
4. <span data-ttu-id="90438-114">Angiv en værdi i feltet Produktnavn.</span><span class="sxs-lookup"><span data-stu-id="90438-114">In the Product name field, type a value.</span></span>
    * <span data-ttu-id="90438-115">Indtast et beskrivende produktnavn.</span><span class="sxs-lookup"><span data-stu-id="90438-115">Enter a descriptive product name.</span></span> <span data-ttu-id="90438-116">Værdien angives som standard til søgenavnet, men dette kan ændres af brugeren.</span><span class="sxs-lookup"><span data-stu-id="90438-116">The value defaults to the search name, but this can be changed by the user.</span></span>  
5. <span data-ttu-id="90438-117">Klik på rullelisten i feltet Produktdimensionsgruppe for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="90438-117">In the Product dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="90438-118">Produktdimensionsgruppen styrer, hvilke af de 4 produktdimensioner der kan bruges til at oprette produktvarianter.</span><span class="sxs-lookup"><span data-stu-id="90438-118">The product dimension group determines which of the 4 product dimensions that can be used to create product variants.</span></span> <span data-ttu-id="90438-119">I dette eksempel bruges en gruppe med farve og størrelse.</span><span class="sxs-lookup"><span data-stu-id="90438-119">This example uses a group with color and size.</span></span>  
6. <span data-ttu-id="90438-120">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="90438-120">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="90438-121">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="90438-121">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="90438-122">Standardkonfigurationsteknologien er en foruddefineret variant.</span><span class="sxs-lookup"><span data-stu-id="90438-122">The default configuration technology is Predefined variant.</span></span> <span data-ttu-id="90438-123">Den vil blive brugt i dette eksempel.</span><span class="sxs-lookup"><span data-stu-id="90438-123">This will be used for this example.</span></span>  
8. <span data-ttu-id="90438-124">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="90438-124">Click OK.</span></span>

## <a name="select-product-dimension-groups"></a><span data-ttu-id="90438-125">Vælg produktdimensionsgrupper</span><span class="sxs-lookup"><span data-stu-id="90438-125">Select product dimension groups</span></span>
1. <span data-ttu-id="90438-126">Klik på rullelisten i feltet Farvegruppe for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="90438-126">In the Color group field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="90438-127">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="90438-127">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="90438-128">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="90438-128">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="90438-129">Klik på rullelisten i feltet Størrelsesgruppe for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="90438-129">In the Size group field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="90438-130">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="90438-130">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="90438-131">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="90438-131">In the list, click the link in the selected row.</span></span>

## <a name="add-dimension-groups"></a><span data-ttu-id="90438-132">Tilføj dimensionsgrupper</span><span class="sxs-lookup"><span data-stu-id="90438-132">Add dimension groups</span></span>
1. <span data-ttu-id="90438-133">Klik på Produkt i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="90438-133">On the Action Pane, click Product.</span></span>
2. <span data-ttu-id="90438-134">Klik på Dimensionsgrupper for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="90438-134">Click Dimension groups to open the drop dialog.</span></span>
3. <span data-ttu-id="90438-135">Klik på rullelisten i feltet Lagringsdimensionsgruppe for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="90438-135">In the Storage dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="90438-136">Lagringsdimensionerne gør det lettere at styre, hvordan varer opbevares og plukkes på lageret.</span><span class="sxs-lookup"><span data-stu-id="90438-136">The storage dimensions help you control how items are stored and taken from inventory.</span></span> <span data-ttu-id="90438-137">For eksempel kan en lagringsdimension omfatte lokation og lagersted.</span><span class="sxs-lookup"><span data-stu-id="90438-137">For example, a storage dimension can include Site and Warehouse.</span></span>  
4. <span data-ttu-id="90438-138">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="90438-138">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="90438-139">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="90438-139">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="90438-140">Klik på rullelisten i feltet Sporingsdimensionsgruppe for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="90438-140">In the Tracking dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="90438-141">Sporingsdimensionsgruppen bestemmer, hvilke sporingsdimensioner du kan føje til et produkt.</span><span class="sxs-lookup"><span data-stu-id="90438-141">The tracking dimension group determines which tracking dimensions you can add to a product.</span></span> <span data-ttu-id="90438-142">For eksempel bruges batchnummeret og serienummeret til at spore lagervarer.</span><span class="sxs-lookup"><span data-stu-id="90438-142">For example, the batch number and serial number are used to track inventory items.</span></span>  
7. <span data-ttu-id="90438-143">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="90438-143">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="90438-144">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="90438-144">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="90438-145">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="90438-145">Click OK.</span></span>
10. <span data-ttu-id="90438-146">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="90438-146">Click Save.</span></span>
11. <span data-ttu-id="90438-147">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="90438-147">Close the page.</span></span>


