---
title: Oprette en stykliste for en dimensionsbaseret produktmaster
description: Til denne procedure skal du har fuldført de foregående 4 vejledninger i denne sekvens på otte optagelser.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, BOMConsistOf, BOMTable, InventItemIdLookupSimple, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: acac36a1078e3f45f59989e62accbc63d596cc26
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3209277"
---
# <a name="create-a-bill-of-materials-for-a-dimension-based-product-master"></a><span data-ttu-id="e438c-103">Oprette en stykliste for en dimensionsbaseret produktmaster</span><span class="sxs-lookup"><span data-stu-id="e438c-103">Create a bill of materials for a dimension-based product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e438c-104">Til denne procedure skal du har fuldført de foregående 4 vejledninger i denne sekvens på otte optagelser.</span><span class="sxs-lookup"><span data-stu-id="e438c-104">For this procedure you should have completed the previous 4 guides in this sequence of eight recordings.</span></span> <span data-ttu-id="e438c-105">De første fire optagelser opsætter de data, der kræves for at fuldføre denne procedure.</span><span class="sxs-lookup"><span data-stu-id="e438c-105">The first 4 recordings set up data that is required to complete this procedure.</span></span> <span data-ttu-id="e438c-106">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="e438c-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="e438c-107">Denne opgave håndteres normalt af produktdesigneren.</span><span class="sxs-lookup"><span data-stu-id="e438c-107">This task is typically handled by the product designer.</span></span>


## <a name="select-the-product"></a><span data-ttu-id="e438c-108">Vælge produktet</span><span class="sxs-lookup"><span data-stu-id="e438c-108">Select the product</span></span>
1. <span data-ttu-id="e438c-109">Klik på Vedligeholdelse af frigivet produkt.</span><span class="sxs-lookup"><span data-stu-id="e438c-109">Click Released product maintenance.</span></span>
2. <span data-ttu-id="e438c-110">Klik på Frigivne produkter.</span><span class="sxs-lookup"><span data-stu-id="e438c-110">Click Released products.</span></span>
3. <span data-ttu-id="e438c-111">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="e438c-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="e438c-112">Find den frigivne produktmasteren med teknologien til dimensionsbaseret konfiguration, som du oprettede i den første opgavevejledning i denne sekvens.</span><span class="sxs-lookup"><span data-stu-id="e438c-112">Find the released product master with dimension-based configuration technology that you created in the first task guide in this sequence.</span></span>  
4. <span data-ttu-id="e438c-113">Klik på Tekniker i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="e438c-113">On the Action Pane, click Engineer.</span></span>
5. <span data-ttu-id="e438c-114">Klik på Styklisteversioner.</span><span class="sxs-lookup"><span data-stu-id="e438c-114">Click BOM versions.</span></span>

## <a name="create-new-bom-and-bom-version"></a><span data-ttu-id="e438c-115">Oprette en ny stykliste og en ny styklisteversion</span><span class="sxs-lookup"><span data-stu-id="e438c-115">Create new BOM and BOM version</span></span>
1. <span data-ttu-id="e438c-116">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="e438c-116">Click New.</span></span>
2. <span data-ttu-id="e438c-117">Klik på Stykliste og Styklisteversion.</span><span class="sxs-lookup"><span data-stu-id="e438c-117">Click BOM and BOM version.</span></span>
3. <span data-ttu-id="e438c-118">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="e438c-118">In the Name field, type a value.</span></span>
    * <span data-ttu-id="e438c-119">Indstilling af en lokation</span><span class="sxs-lookup"><span data-stu-id="e438c-119">Setting a site</span></span>  
    * <span data-ttu-id="e438c-120">Vi angiver ikke en specifik lokation for styklisten i denne procedure.</span><span class="sxs-lookup"><span data-stu-id="e438c-120">In this procedure we don't set a specific site for the BOM.</span></span>  
4. <span data-ttu-id="e438c-121">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="e438c-121">Click OK.</span></span>
5. <span data-ttu-id="e438c-122">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="e438c-122">Click New.</span></span>
    * <span data-ttu-id="e438c-123">I denne procedure vil vi tilføje fire linjer til styklisten.</span><span class="sxs-lookup"><span data-stu-id="e438c-123">In this procedure we will add four lines to the BOM.</span></span> <span data-ttu-id="e438c-124">To linjer repræsenterer kabelindstillinger, og to linjer repræsenterer kabinetindstillinger.</span><span class="sxs-lookup"><span data-stu-id="e438c-124">Two lines represent cable options and two lines represent cabinet options.</span></span>  
6. <span data-ttu-id="e438c-125">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="e438c-125">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="e438c-126">Indtast eller vælg en værdi i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="e438c-126">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="e438c-127">Vælg varenummeret A0001, HDMI 6'-kabler.</span><span class="sxs-lookup"><span data-stu-id="e438c-127">Select item number A0001, HDMI 6' Cables.</span></span>  
8. <span data-ttu-id="e438c-128">Indtast eller vælg en værdi i feltet Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="e438c-128">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="e438c-129">Vælg den kabelvariantgruppe, der blev oprettet i vejledning 4 i denne sekvens.</span><span class="sxs-lookup"><span data-stu-id="e438c-129">Select the Cable configuration group created in guide 4 in this sequence.</span></span>  
9. <span data-ttu-id="e438c-130">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="e438c-130">Click New.</span></span>
    * <span data-ttu-id="e438c-131">Vælg varenummeret A0002, HDMI 12'-kabler.</span><span class="sxs-lookup"><span data-stu-id="e438c-131">Select item number A0002, HDMI 12' Cables.</span></span>  
10. <span data-ttu-id="e438c-132">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="e438c-132">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="e438c-133">Indtast eller vælg en værdi i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="e438c-133">In the Item number field, enter or select a value.</span></span>
12. <span data-ttu-id="e438c-134">Indtast eller vælg en værdi i feltet Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="e438c-134">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="e438c-135">Vælg igen variantgruppen Kabel.</span><span class="sxs-lookup"><span data-stu-id="e438c-135">Select the Cable configuration group again.</span></span>  
13. <span data-ttu-id="e438c-136">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="e438c-136">Click New.</span></span>
14. <span data-ttu-id="e438c-137">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="e438c-137">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="e438c-138">Indtast eller vælg en værdi i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="e438c-138">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="e438c-139">Vælg varenummeret D0002 Kabinet.</span><span class="sxs-lookup"><span data-stu-id="e438c-139">Select item number D0002 Cabinet.</span></span>  
16. <span data-ttu-id="e438c-140">Indtast eller vælg en værdi i feltet Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="e438c-140">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="e438c-141">Vælg variantgruppen Kabinet til denne styklistelinje.</span><span class="sxs-lookup"><span data-stu-id="e438c-141">Select the Cabinet configuration group for this BOM line.</span></span>  
17. <span data-ttu-id="e438c-142">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="e438c-142">Click New.</span></span>
18. <span data-ttu-id="e438c-143">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="e438c-143">In the list, mark the selected row.</span></span>
19. <span data-ttu-id="e438c-144">Indtast eller vælg en værdi i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="e438c-144">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="e438c-145">Vælg varenummeret M0007 Standardkabinet som den sidste styklistelinje.</span><span class="sxs-lookup"><span data-stu-id="e438c-145">Select Item number M0007 StandardCabinet as the last BOM line.</span></span>  
20. <span data-ttu-id="e438c-146">Indtast eller vælg en værdi i feltet Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="e438c-146">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="e438c-147">Vælg variantgruppen Kabinet til den sidste styklistelinje.</span><span class="sxs-lookup"><span data-stu-id="e438c-147">Select the Cabinet configuration group for the laste BOM line.</span></span>  

## <a name="approve-and-activate"></a><span data-ttu-id="e438c-148">Godkend og aktivér</span><span class="sxs-lookup"><span data-stu-id="e438c-148">Approve and activate</span></span>
1. <span data-ttu-id="e438c-149">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="e438c-149">Close the page.</span></span>
2. <span data-ttu-id="e438c-150">Klik på Godkend.</span><span class="sxs-lookup"><span data-stu-id="e438c-150">Click Approve.</span></span>
3. <span data-ttu-id="e438c-151">Indtast eller vælg en værdi i feltet Godkendt af.</span><span class="sxs-lookup"><span data-stu-id="e438c-151">In the Approved by field, enter or select a value.</span></span>
4. <span data-ttu-id="e438c-152">Vælg Ja til Vil du også godkende styklisten? .</span><span class="sxs-lookup"><span data-stu-id="e438c-152">Select Yes in the Do you also want to approve the bill of materials? field.</span></span>
5. <span data-ttu-id="e438c-153">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="e438c-153">Click OK.</span></span>
6. <span data-ttu-id="e438c-154">Klik på Aktiver.</span><span class="sxs-lookup"><span data-stu-id="e438c-154">Click Activate.</span></span>

