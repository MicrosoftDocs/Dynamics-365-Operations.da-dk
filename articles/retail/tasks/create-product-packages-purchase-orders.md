--- 
title: " Oprette produktpakker til indkøbsordrer"
description: "Denne procedure gennemgår oprettelse af en produktpakke og brugen af den i en indkøbsordre."
author: josaw1
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
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: a3be1e7aca7f0382aea55fa8a371c33c8b53df95
ms.contentlocale: da-dk
ms.lasthandoff: 08/29/2017

---
# <a name="create-product-packages-for-purchase-orders"></a><span data-ttu-id="f2201-103"> Oprette produktpakker til indkøbsordrer</span><span class="sxs-lookup"><span data-stu-id="f2201-103">Create product packages for purchase orders</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="f2201-104">Denne procedure gennemgår oprettelse af en produktpakke og brugen af den i en indkøbsordre.</span><span class="sxs-lookup"><span data-stu-id="f2201-104">This procedure walks through creating a product package and using it on a purchase order.</span></span> <span data-ttu-id="f2201-105">Indkøbsordren skal bruges til at oprette en ordre på et foruddefineret sæt produkter.</span><span class="sxs-lookup"><span data-stu-id="f2201-105">The purchase order will be used to create an order for a pre-defined set of products.</span></span> <span data-ttu-id="f2201-106">Proceduren bruger USRT-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="f2201-106">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-product-package"></a><span data-ttu-id="f2201-107">Oprette en produktpakke</span><span class="sxs-lookup"><span data-stu-id="f2201-107">Create a product package</span></span>
1. <span data-ttu-id="f2201-108">Gå til Detail og handel > Lagerstyring > Opfyldning > Produktpakker.</span><span class="sxs-lookup"><span data-stu-id="f2201-108">Go to Retail and commerce > Inventory management > Replenishment > Product packages.</span></span>
2. <span data-ttu-id="f2201-109">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="f2201-109">Click New.</span></span>
3. <span data-ttu-id="f2201-110">Skriv en værdi i feltet Pakkenummer.</span><span class="sxs-lookup"><span data-stu-id="f2201-110">In the Package number field, type a value.</span></span>
4. <span data-ttu-id="f2201-111">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="f2201-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="f2201-112">Klik på rullelisten i feltet Kreditorkonto for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="f2201-112">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="f2201-113">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="f2201-113">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="f2201-114">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="f2201-114">Click Add.</span></span>
8. <span data-ttu-id="f2201-115">I feltet Varenummer skal du skrive "0160".</span><span class="sxs-lookup"><span data-stu-id="f2201-115">In the Item number field, type '0160'.</span></span>
9. <span data-ttu-id="f2201-116">Klik på rullelisten i feltet Størrelse for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="f2201-116">In the Size field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="f2201-117">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="f2201-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="f2201-118">Angiv et tal i feltet Antal.</span><span class="sxs-lookup"><span data-stu-id="f2201-118">In the Quantity field, enter a number.</span></span>
12. <span data-ttu-id="f2201-119">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="f2201-119">Click Add.</span></span>
13. <span data-ttu-id="f2201-120">I feltet Varenummer skal du skrive "0160".</span><span class="sxs-lookup"><span data-stu-id="f2201-120">In the Item number field, type '0160'.</span></span>
14. <span data-ttu-id="f2201-121">Klik på rullelisten i feltet Variantnummer for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="f2201-121">In the Variant number field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="f2201-122">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="f2201-122">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="f2201-123">Angiv et tal i feltet Antal.</span><span class="sxs-lookup"><span data-stu-id="f2201-123">In the Quantity field, enter a number.</span></span>
17. <span data-ttu-id="f2201-124">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="f2201-124">Click Add.</span></span>
18. <span data-ttu-id="f2201-125">I feltet Varenummer skal du skrive "0175".</span><span class="sxs-lookup"><span data-stu-id="f2201-125">In the Item number field, type '0175'.</span></span>
19. <span data-ttu-id="f2201-126">Angiv et tal i feltet Antal.</span><span class="sxs-lookup"><span data-stu-id="f2201-126">In the Quantity field, enter a number.</span></span>
20. <span data-ttu-id="f2201-127">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="f2201-127">Click Save.</span></span>
21. <span data-ttu-id="f2201-128">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="f2201-128">Close the page.</span></span>

## <a name="add-package-to-puchase-order"></a><span data-ttu-id="f2201-129">Føje pakke til indkøbsordre</span><span class="sxs-lookup"><span data-stu-id="f2201-129">Add package to puchase order</span></span>
1. <span data-ttu-id="f2201-130">Gå til Kreditor > Indkøbsordrer > Alle indkøbsordrer.</span><span class="sxs-lookup"><span data-stu-id="f2201-130">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="f2201-131">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="f2201-131">Click New.</span></span>
3. <span data-ttu-id="f2201-132">Klik på rullelisten i feltet Kreditorkonto for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="f2201-132">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="f2201-133">Vælg den samme leverandør, som produktpakken tidligere blev oprettet for, på listen, hvis der blev valgt en leverandør.</span><span class="sxs-lookup"><span data-stu-id="f2201-133">In the list, select the same vendor that the product package was previously created for, if a vendor was selected.</span></span>
5. <span data-ttu-id="f2201-134">Slå udvidelsen af sektionen Generelt til/fra.</span><span class="sxs-lookup"><span data-stu-id="f2201-134">Toggle the expansion of the General section.</span></span>
6. <span data-ttu-id="f2201-135">Klik på rullelisten i feltet Sted for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="f2201-135">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="f2201-136">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="f2201-136">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="f2201-137">Klik på rullelisten i feltet Lagersted for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="f2201-137">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="f2201-138">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="f2201-138">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="f2201-139">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="f2201-139">Click OK.</span></span>
11. <span data-ttu-id="f2201-140">Slå udvidelsen af sektionen Linjedetaljer til/fra.</span><span class="sxs-lookup"><span data-stu-id="f2201-140">Toggle the expansion of the Line details section.</span></span>
12. <span data-ttu-id="f2201-141">Klik på fanen Produktpakker.</span><span class="sxs-lookup"><span data-stu-id="f2201-141">Click the Product packages tab.</span></span>
13. <span data-ttu-id="f2201-142">Klik på Indkøbsordrelinje.</span><span class="sxs-lookup"><span data-stu-id="f2201-142">Click Purchase order line.</span></span>
14. <span data-ttu-id="f2201-143">Klik på Opret linjer fra pakke.</span><span class="sxs-lookup"><span data-stu-id="f2201-143">Click Create lines from package.</span></span>
15. <span data-ttu-id="f2201-144">Find og vælg på listen den produktpakke, der blev oprettet i forrige trin.</span><span class="sxs-lookup"><span data-stu-id="f2201-144">In the list, find and select the product package created in previous step.</span></span>
16. <span data-ttu-id="f2201-145">Angiv et tal i feltet Antal.</span><span class="sxs-lookup"><span data-stu-id="f2201-145">In the Quantity field, enter a number.</span></span>
17. <span data-ttu-id="f2201-146">Klik på Opret.</span><span class="sxs-lookup"><span data-stu-id="f2201-146">Click Create.</span></span>
18. <span data-ttu-id="f2201-147">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="f2201-147">Click Save.</span></span>


