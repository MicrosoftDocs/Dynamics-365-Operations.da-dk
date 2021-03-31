---
title: Oprette en produktmaster
description: Opret en produktmaster for de foruddefinerede varianter.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d580d323409d84bab66dc03d39e084f5ee0cfc64
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5218483"
---
# <a name="create-a-product-master"></a><span data-ttu-id="9f87d-103">Oprette en produktmaster</span><span class="sxs-lookup"><span data-stu-id="9f87d-103">Create a product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9f87d-104">Opret en produktmaster for de foruddefinerede varianter.</span><span class="sxs-lookup"><span data-stu-id="9f87d-104">Create a product master for the predefined variants.</span></span> <span data-ttu-id="9f87d-105">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="9f87d-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="9f87d-106">Denne procedure er beregnet til produktdesigneren.</span><span class="sxs-lookup"><span data-stu-id="9f87d-106">This procedure is intended for the product designer.</span></span>


## <a name="create-a-new-product-master"></a><span data-ttu-id="9f87d-107">Opret en ny produktmaster</span><span class="sxs-lookup"><span data-stu-id="9f87d-107">Create a new product master</span></span>
1. <span data-ttu-id="9f87d-108">Gå til **Navigationsrude > Moduler > Administration af produktoplysninger > Produkter > Produktmastere**.</span><span class="sxs-lookup"><span data-stu-id="9f87d-108">Go to **Navigation pane > Modules > Product information management > Products > Product masters**.</span></span>
2. <span data-ttu-id="9f87d-109">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="9f87d-109">Click **New**.</span></span>
3. <span data-ttu-id="9f87d-110">Skriv en værdi i feltet **Produktnummer**.</span><span class="sxs-lookup"><span data-stu-id="9f87d-110">In the **Product number** field, type a value.</span></span> <span data-ttu-id="9f87d-111">Tallet skal være entydigt.</span><span class="sxs-lookup"><span data-stu-id="9f87d-111">The number must be unique.</span></span> <span data-ttu-id="9f87d-112">En nummerserie kan konfigureres for feltet **Produktnummer**.</span><span class="sxs-lookup"><span data-stu-id="9f87d-112">A number sequence can be set for the **Product number** field.</span></span> <span data-ttu-id="9f87d-113">I dette tilfælde skal brugeren ikke at angive en værdi.</span><span class="sxs-lookup"><span data-stu-id="9f87d-113">In this case, the user doesn't have to enter a value.</span></span>
4. <span data-ttu-id="9f87d-114">Skriv en værdi i feltet **Produktnavn**.</span><span class="sxs-lookup"><span data-stu-id="9f87d-114">In the **Product name** field, type a value.</span></span> <span data-ttu-id="9f87d-115">Indtast et beskrivende produktnavn.</span><span class="sxs-lookup"><span data-stu-id="9f87d-115">Enter a descriptive product name.</span></span> <span data-ttu-id="9f87d-116">Værdien angives som standard til søgenavnet, men dette kan ændres af brugeren.</span><span class="sxs-lookup"><span data-stu-id="9f87d-116">The value defaults to the search name, but this can be changed by the user.</span></span>
5. <span data-ttu-id="9f87d-117">Klik på rullelisten i feltet **Produktdimensionsgruppe** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="9f87d-117">In the **Product dimension group** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="9f87d-118">Produktdimensionsgruppen styrer, hvilke af de 4 produktdimensioner der kan bruges til at oprette produktvarianter.</span><span class="sxs-lookup"><span data-stu-id="9f87d-118">The product dimension group determines which of the 4 product dimensions that can be used to create product variants.</span></span> <span data-ttu-id="9f87d-119">I dette eksempel bruges en gruppe med farve og størrelse.</span><span class="sxs-lookup"><span data-stu-id="9f87d-119">This example uses a group with color and size.</span></span>
6. <span data-ttu-id="9f87d-120">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="9f87d-120">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="9f87d-121">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="9f87d-121">In the list, click the link in the selected row.</span></span> <span data-ttu-id="9f87d-122">Standarden **Konfigurationsteknologi** er 'Foruddefineret variant'.</span><span class="sxs-lookup"><span data-stu-id="9f87d-122">The default **Configuration technology** is 'Predefined variant'.</span></span> <span data-ttu-id="9f87d-123">Den vil blive brugt i dette eksempel.</span><span class="sxs-lookup"><span data-stu-id="9f87d-123">This will be used for this example.</span></span>
8. <span data-ttu-id="9f87d-124">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="9f87d-124">Click **OK**.</span></span>

## <a name="select-product-dimension-groups"></a><span data-ttu-id="9f87d-125">Vælg produktdimensionsgrupper</span><span class="sxs-lookup"><span data-stu-id="9f87d-125">Select product dimension groups</span></span>
1. <span data-ttu-id="9f87d-126">Klik på rullelisten i feltet **Farvegruppe** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="9f87d-126">In the **Color group** field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="9f87d-127">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="9f87d-127">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="9f87d-128">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="9f87d-128">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="9f87d-129">Klik på rullelisten i feltet **Størrelsesgruppe** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="9f87d-129">In the **Size group** field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="9f87d-130">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="9f87d-130">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="9f87d-131">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="9f87d-131">In the list, click the link in the selected row.</span></span>

## <a name="add-dimension-groups"></a><span data-ttu-id="9f87d-132">Tilføj dimensionsgrupper</span><span class="sxs-lookup"><span data-stu-id="9f87d-132">Add dimension groups</span></span>
1. <span data-ttu-id="9f87d-133">Klik på **Produkt** i **handlingsruden**.</span><span class="sxs-lookup"><span data-stu-id="9f87d-133">On the **Action Pane**, click **Product**.</span></span>
2. <span data-ttu-id="9f87d-134">Klik på **Dimensionsgrupper** for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="9f87d-134">Click **Dimension groups** to open the drop dialog.</span></span>
3. <span data-ttu-id="9f87d-135">Klik på rullelisten i feltet **Lagringsdimensionsgruppe** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="9f87d-135">In the **Storage dimension group** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="9f87d-136">Lagringsdimensionerne gør det lettere at styre, hvordan varer opbevares og plukkes på lageret.</span><span class="sxs-lookup"><span data-stu-id="9f87d-136">The storage dimensions help you control how items are stored and taken from inventory.</span></span> <span data-ttu-id="9f87d-137">For eksempel kan en lagringsdimension omfatte lokation og lagersted.</span><span class="sxs-lookup"><span data-stu-id="9f87d-137">For example, a storage dimension can include Site and Warehouse.</span></span>
4. <span data-ttu-id="9f87d-138">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="9f87d-138">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="9f87d-139">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="9f87d-139">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="9f87d-140">Klik på rullelisten i feltet **Sporingsdimensionsgruppe** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="9f87d-140">In the **Tracking dimension group** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="9f87d-141">Sporingsdimensionsgruppen bestemmer, hvilke sporingsdimensioner du kan føje til et produkt.</span><span class="sxs-lookup"><span data-stu-id="9f87d-141">The tracking dimension group determines which tracking dimensions you can add to a product.</span></span> <span data-ttu-id="9f87d-142">For eksempel bruges batchnummeret og serienummeret til at spore lagervarer.</span><span class="sxs-lookup"><span data-stu-id="9f87d-142">For example, the batch number and serial number are used to track inventory items.</span></span>
7. <span data-ttu-id="9f87d-143">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="9f87d-143">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="9f87d-144">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="9f87d-144">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="9f87d-145">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="9f87d-145">Click **OK**.</span></span>
10. <span data-ttu-id="9f87d-146">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="9f87d-146">Click **Save**.</span></span>
11. <span data-ttu-id="9f87d-147">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="9f87d-147">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]