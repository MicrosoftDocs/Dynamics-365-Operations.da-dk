---
title: " Oprette produktpakker til indkøbsordrer"
description: Denne procedure gennemgår oprettelse af en produktpakke og brugen af den i en indkøbsordre.
author: josaw1
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 296b3fb03b20dee5b6024c182df7feb3ce280913
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4964664"
---
# <a name="create-product-packages-for-purchase-orders"></a><span data-ttu-id="c4b0d-103"> Oprette produktpakker til indkøbsordrer</span><span class="sxs-lookup"><span data-stu-id="c4b0d-103">Create product packages for purchase orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c4b0d-104">Denne procedure gennemgår oprettelse af en produktpakke og brugen af den i en indkøbsordre.</span><span class="sxs-lookup"><span data-stu-id="c4b0d-104">This procedure walks through creating a product package and using it on a purchase order.</span></span> <span data-ttu-id="c4b0d-105">Indkøbsordren skal bruges til at oprette en ordre på et foruddefineret sæt produkter.</span><span class="sxs-lookup"><span data-stu-id="c4b0d-105">The purchase order will be used to create an order for a pre-defined set of products.</span></span> <span data-ttu-id="c4b0d-106">Proceduren bruger USRT-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="c4b0d-106">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-product-package"></a><span data-ttu-id="c4b0d-107">Oprette en produktpakke</span><span class="sxs-lookup"><span data-stu-id="c4b0d-107">Create a product package</span></span>
1. <span data-ttu-id="c4b0d-108">Gå til Retail og Commerce > Lagerstyring > Genopfyldning > Produktpakker.</span><span class="sxs-lookup"><span data-stu-id="c4b0d-108">Go to Retail and Commerce > Inventory management > Replenishment > Product packages.</span></span>
2. <span data-ttu-id="c4b0d-109">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="c4b0d-109">Click New.</span></span>
3. <span data-ttu-id="c4b0d-110">Skriv en værdi i feltet Pakkenummer.</span><span class="sxs-lookup"><span data-stu-id="c4b0d-110">In the Package number field, type a value.</span></span>
4. <span data-ttu-id="c4b0d-111">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="c4b0d-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="c4b0d-112">Klik på rullelisten i feltet Kreditorkonto for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="c4b0d-112">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="c4b0d-113">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="c4b0d-113">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="c4b0d-114">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="c4b0d-114">Click Add.</span></span>
8. <span data-ttu-id="c4b0d-115">I feltet Varenummer skal du skrive "0160".</span><span class="sxs-lookup"><span data-stu-id="c4b0d-115">In the Item number field, type '0160'.</span></span>
9. <span data-ttu-id="c4b0d-116">Klik på rullelisten i feltet Størrelse for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="c4b0d-116">In the Size field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="c4b0d-117">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="c4b0d-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="c4b0d-118">Angiv et tal i feltet Antal.</span><span class="sxs-lookup"><span data-stu-id="c4b0d-118">In the Quantity field, enter a number.</span></span>
12. <span data-ttu-id="c4b0d-119">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="c4b0d-119">Click Add.</span></span>
13. <span data-ttu-id="c4b0d-120">I feltet Varenummer skal du skrive "0160".</span><span class="sxs-lookup"><span data-stu-id="c4b0d-120">In the Item number field, type '0160'.</span></span>
14. <span data-ttu-id="c4b0d-121">Klik på rullelisten i feltet Variantnummer for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="c4b0d-121">In the Variant number field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="c4b0d-122">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="c4b0d-122">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="c4b0d-123">Angiv et tal i feltet Antal.</span><span class="sxs-lookup"><span data-stu-id="c4b0d-123">In the Quantity field, enter a number.</span></span>
17. <span data-ttu-id="c4b0d-124">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="c4b0d-124">Click Add.</span></span>
18. <span data-ttu-id="c4b0d-125">I feltet Varenummer skal du skrive "0175".</span><span class="sxs-lookup"><span data-stu-id="c4b0d-125">In the Item number field, type '0175'.</span></span>
19. <span data-ttu-id="c4b0d-126">Angiv et tal i feltet Antal.</span><span class="sxs-lookup"><span data-stu-id="c4b0d-126">In the Quantity field, enter a number.</span></span>
20. <span data-ttu-id="c4b0d-127">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="c4b0d-127">Click Save.</span></span>
21. <span data-ttu-id="c4b0d-128">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="c4b0d-128">Close the page.</span></span>

## <a name="add-package-to-purchase-order"></a><span data-ttu-id="c4b0d-129">Føje pakke til indkøbsordre</span><span class="sxs-lookup"><span data-stu-id="c4b0d-129">Add package to purchase order</span></span>
1. <span data-ttu-id="c4b0d-130">Gå til Kreditor > Indkøbsordrer > Alle indkøbsordrer.</span><span class="sxs-lookup"><span data-stu-id="c4b0d-130">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="c4b0d-131">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="c4b0d-131">Click New.</span></span>
3. <span data-ttu-id="c4b0d-132">Klik på rullelisten i feltet Kreditorkonto for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="c4b0d-132">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="c4b0d-133">Vælg den samme leverandør, som produktpakken tidligere blev oprettet for, på listen, hvis der blev valgt en leverandør.</span><span class="sxs-lookup"><span data-stu-id="c4b0d-133">In the list, select the same vendor that the product package was previously created for, if a vendor was selected.</span></span>
5. <span data-ttu-id="c4b0d-134">Slå udvidelsen af sektionen Generelt til/fra.</span><span class="sxs-lookup"><span data-stu-id="c4b0d-134">Toggle the expansion of the General section.</span></span>
6. <span data-ttu-id="c4b0d-135">Klik på rullelisten i feltet Sted for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="c4b0d-135">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="c4b0d-136">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="c4b0d-136">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="c4b0d-137">Klik på rullelisten i feltet Lagersted for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="c4b0d-137">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="c4b0d-138">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="c4b0d-138">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="c4b0d-139">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="c4b0d-139">Click OK.</span></span>
11. <span data-ttu-id="c4b0d-140">Slå udvidelsen af sektionen Linjedetaljer til/fra.</span><span class="sxs-lookup"><span data-stu-id="c4b0d-140">Toggle the expansion of the Line details section.</span></span>
12. <span data-ttu-id="c4b0d-141">Klik på fanen Produktpakker.</span><span class="sxs-lookup"><span data-stu-id="c4b0d-141">Click the Product packages tab.</span></span>
13. <span data-ttu-id="c4b0d-142">Klik på Indkøbsordrelinje.</span><span class="sxs-lookup"><span data-stu-id="c4b0d-142">Click Purchase order line.</span></span>
14. <span data-ttu-id="c4b0d-143">Klik på Opret linjer fra pakke.</span><span class="sxs-lookup"><span data-stu-id="c4b0d-143">Click Create lines from package.</span></span>
15. <span data-ttu-id="c4b0d-144">Find og vælg på listen den produktpakke, der blev oprettet i forrige trin.</span><span class="sxs-lookup"><span data-stu-id="c4b0d-144">In the list, find and select the product package created in previous step.</span></span>
16. <span data-ttu-id="c4b0d-145">Angiv et tal i feltet Antal.</span><span class="sxs-lookup"><span data-stu-id="c4b0d-145">In the Quantity field, enter a number.</span></span>
17. <span data-ttu-id="c4b0d-146">Klik på Opret.</span><span class="sxs-lookup"><span data-stu-id="c4b0d-146">Click Create.</span></span>
18. <span data-ttu-id="c4b0d-147">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="c4b0d-147">Click Save.</span></span>

