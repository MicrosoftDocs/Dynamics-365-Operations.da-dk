---
title: Oprette en produktmaster
description: Opret en produktmaster for de foruddefinerede varianter.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 70008e903763fff35c6cff12c42396fe5fcabbee
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832076"
---
# <a name="create-a-product-master"></a><span data-ttu-id="ed211-103">Oprette en produktmaster</span><span class="sxs-lookup"><span data-stu-id="ed211-103">Create a product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ed211-104">Opret en produktmaster for de foruddefinerede varianter.</span><span class="sxs-lookup"><span data-stu-id="ed211-104">Create a product master for the predefined variants.</span></span> <span data-ttu-id="ed211-105">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="ed211-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="ed211-106">Denne procedure er beregnet til produktdesigneren.</span><span class="sxs-lookup"><span data-stu-id="ed211-106">This procedure is intended for the product designer.</span></span>


## <a name="create-a-new-product-master"></a><span data-ttu-id="ed211-107">Opret en ny produktmaster</span><span class="sxs-lookup"><span data-stu-id="ed211-107">Create a new product master</span></span>
1. <span data-ttu-id="ed211-108">Gå til **Navigationsrude > Moduler > Administration af produktoplysninger > Produkter > Produktmastere**.</span><span class="sxs-lookup"><span data-stu-id="ed211-108">Go to **Navigation pane > Modules > Product information management > Products > Product masters**.</span></span>
2. <span data-ttu-id="ed211-109">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="ed211-109">Click **New**.</span></span>
3. <span data-ttu-id="ed211-110">Skriv en værdi i feltet **Produktnummer**.</span><span class="sxs-lookup"><span data-stu-id="ed211-110">In the **Product number** field, type a value.</span></span> <span data-ttu-id="ed211-111">Tallet skal være entydigt.</span><span class="sxs-lookup"><span data-stu-id="ed211-111">The number must be unique.</span></span> <span data-ttu-id="ed211-112">En nummerserie kan konfigureres for feltet **Produktnummer**.</span><span class="sxs-lookup"><span data-stu-id="ed211-112">A number sequence can be set for the **Product number** field.</span></span> <span data-ttu-id="ed211-113">I dette tilfælde skal brugeren ikke at angive en værdi.</span><span class="sxs-lookup"><span data-stu-id="ed211-113">In this case, the user doesn't have to enter a value.</span></span>
4. <span data-ttu-id="ed211-114">Skriv en værdi i feltet **Produktnavn**.</span><span class="sxs-lookup"><span data-stu-id="ed211-114">In the **Product name** field, type a value.</span></span> <span data-ttu-id="ed211-115">Indtast et beskrivende produktnavn.</span><span class="sxs-lookup"><span data-stu-id="ed211-115">Enter a descriptive product name.</span></span> <span data-ttu-id="ed211-116">Værdien angives som standard til søgenavnet, men dette kan ændres af brugeren.</span><span class="sxs-lookup"><span data-stu-id="ed211-116">The value defaults to the search name, but this can be changed by the user.</span></span>
5. <span data-ttu-id="ed211-117">Klik på rullelisten i feltet **Produktdimensionsgruppe** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="ed211-117">In the **Product dimension group** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="ed211-118">Produktdimensionsgruppen styrer, hvilke af de 4 produktdimensioner der kan bruges til at oprette produktvarianter.</span><span class="sxs-lookup"><span data-stu-id="ed211-118">The product dimension group determines which of the 4 product dimensions that can be used to create product variants.</span></span> <span data-ttu-id="ed211-119">I dette eksempel bruges en gruppe med farve og størrelse.</span><span class="sxs-lookup"><span data-stu-id="ed211-119">This example uses a group with color and size.</span></span>
6. <span data-ttu-id="ed211-120">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="ed211-120">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="ed211-121">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="ed211-121">In the list, click the link in the selected row.</span></span> <span data-ttu-id="ed211-122">Standarden **Konfigurationsteknologi** er 'Foruddefineret variant'.</span><span class="sxs-lookup"><span data-stu-id="ed211-122">The default **Configuration technology** is 'Predefined variant'.</span></span> <span data-ttu-id="ed211-123">Den vil blive brugt i dette eksempel.</span><span class="sxs-lookup"><span data-stu-id="ed211-123">This will be used for this example.</span></span>
8. <span data-ttu-id="ed211-124">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="ed211-124">Click **OK**.</span></span>

## <a name="select-product-dimension-groups"></a><span data-ttu-id="ed211-125">Vælg produktdimensionsgrupper</span><span class="sxs-lookup"><span data-stu-id="ed211-125">Select product dimension groups</span></span>
1. <span data-ttu-id="ed211-126">Klik på rullelisten i feltet **Farvegruppe** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="ed211-126">In the **Color group** field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="ed211-127">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="ed211-127">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="ed211-128">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="ed211-128">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="ed211-129">Klik på rullelisten i feltet **Størrelsesgruppe** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="ed211-129">In the **Size group** field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="ed211-130">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="ed211-130">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="ed211-131">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="ed211-131">In the list, click the link in the selected row.</span></span>

## <a name="add-dimension-groups"></a><span data-ttu-id="ed211-132">Tilføj dimensionsgrupper</span><span class="sxs-lookup"><span data-stu-id="ed211-132">Add dimension groups</span></span>
1. <span data-ttu-id="ed211-133">Klik på **Produkt** i **handlingsruden**.</span><span class="sxs-lookup"><span data-stu-id="ed211-133">On the **Action Pane**, click **Product**.</span></span>
2. <span data-ttu-id="ed211-134">Klik på **Dimensionsgrupper** for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="ed211-134">Click **Dimension groups** to open the drop dialog.</span></span>
3. <span data-ttu-id="ed211-135">Klik på rullelisten i feltet **Lagringsdimensionsgruppe** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="ed211-135">In the **Storage dimension group** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="ed211-136">Lagringsdimensionerne gør det lettere at styre, hvordan varer opbevares og plukkes på lageret.</span><span class="sxs-lookup"><span data-stu-id="ed211-136">The storage dimensions help you control how items are stored and taken from inventory.</span></span> <span data-ttu-id="ed211-137">For eksempel kan en lagringsdimension omfatte lokation og lagersted.</span><span class="sxs-lookup"><span data-stu-id="ed211-137">For example, a storage dimension can include Site and Warehouse.</span></span>
4. <span data-ttu-id="ed211-138">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="ed211-138">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="ed211-139">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="ed211-139">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="ed211-140">Klik på rullelisten i feltet **Sporingsdimensionsgruppe** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="ed211-140">In the **Tracking dimension group** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="ed211-141">Sporingsdimensionsgruppen bestemmer, hvilke sporingsdimensioner du kan føje til et produkt.</span><span class="sxs-lookup"><span data-stu-id="ed211-141">The tracking dimension group determines which tracking dimensions you can add to a product.</span></span> <span data-ttu-id="ed211-142">For eksempel bruges batchnummeret og serienummeret til at spore lagervarer.</span><span class="sxs-lookup"><span data-stu-id="ed211-142">For example, the batch number and serial number are used to track inventory items.</span></span>
7. <span data-ttu-id="ed211-143">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="ed211-143">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="ed211-144">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="ed211-144">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="ed211-145">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="ed211-145">Click **OK**.</span></span>
10. <span data-ttu-id="ed211-146">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="ed211-146">Click **Save**.</span></span>
11. <span data-ttu-id="ed211-147">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="ed211-147">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]