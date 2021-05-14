---
title: Oprette en stykliste for en dimensionsbaseret produktmaster
description: Til denne procedure skal du har fuldført de foregående 4 vejledninger i denne sekvens på otte optagelser.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, BOMConsistOf, BOMTable, InventItemIdLookupSimple, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 13053dd87242963586678b46c64493feb3383c4c
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920699"
---
# <a name="create-a-bill-of-materials-for-a-dimension-based-product-master"></a><span data-ttu-id="67d61-103">Oprette en stykliste for en dimensionsbaseret produktmaster</span><span class="sxs-lookup"><span data-stu-id="67d61-103">Create a bill of materials for a dimension-based product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="67d61-104">Til denne procedure skal du har fuldført de foregående 4 vejledninger i denne sekvens på otte optagelser.</span><span class="sxs-lookup"><span data-stu-id="67d61-104">For this procedure you should have completed the previous 4 guides in this sequence of eight recordings.</span></span> <span data-ttu-id="67d61-105">De første fire optagelser opsætter de data, der kræves for at fuldføre denne procedure.</span><span class="sxs-lookup"><span data-stu-id="67d61-105">The first 4 recordings set up data that is required to complete this procedure.</span></span> <span data-ttu-id="67d61-106">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="67d61-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="67d61-107">Denne opgave håndteres normalt af produktdesigneren.</span><span class="sxs-lookup"><span data-stu-id="67d61-107">This task is typically handled by the product designer.</span></span>

## <a name="select-the-product"></a><span data-ttu-id="67d61-108">Vælge produktet</span><span class="sxs-lookup"><span data-stu-id="67d61-108">Select the product</span></span>

1. <span data-ttu-id="67d61-109">Gå til **Administration af produktoplysninger \> Produkter \> Frigivne produkter**.</span><span class="sxs-lookup"><span data-stu-id="67d61-109">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="67d61-110">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="67d61-110">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="67d61-111">Find den frigivne produktmasteren med teknologien til dimensionsbaseret konfiguration, som du oprettede i den første opgavevejledning i denne sekvens.</span><span class="sxs-lookup"><span data-stu-id="67d61-111">Find the released product master with dimension-based configuration technology that you created in the first task guide in this sequence.</span></span>  
1. <span data-ttu-id="67d61-112">Vælg **Tekniker** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="67d61-112">On the Action Pane, select **Engineer**.</span></span>
1. <span data-ttu-id="67d61-113">Vælg **Styklisteversioner**.</span><span class="sxs-lookup"><span data-stu-id="67d61-113">Select **BOM versions**.</span></span>

## <a name="create-new-bom-and-bom-version"></a><span data-ttu-id="67d61-114">Oprette en ny stykliste og en ny styklisteversion</span><span class="sxs-lookup"><span data-stu-id="67d61-114">Create new BOM and BOM version</span></span>

1. <span data-ttu-id="67d61-115">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="67d61-115">Select **New**.</span></span>
1. <span data-ttu-id="67d61-116">Vælg **Stykliste og styklisteversion**.</span><span class="sxs-lookup"><span data-stu-id="67d61-116">Select **BOM and BOM version**.</span></span>
1. <span data-ttu-id="67d61-117">Skriv en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="67d61-117">In the **Name** field, type a value.</span></span>
    * <span data-ttu-id="67d61-118">Indstilling af en lokation</span><span class="sxs-lookup"><span data-stu-id="67d61-118">Setting a site</span></span>  
    * <span data-ttu-id="67d61-119">Vi angiver ikke en specifik lokation for styklisten i denne procedure.</span><span class="sxs-lookup"><span data-stu-id="67d61-119">In this procedure we don't set a specific site for the BOM.</span></span>  
1. <span data-ttu-id="67d61-120">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="67d61-120">Select **OK**.</span></span>
1. <span data-ttu-id="67d61-121">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="67d61-121">Select **New**.</span></span>
    * <span data-ttu-id="67d61-122">I denne procedure vil vi tilføje fire linjer til styklisten.</span><span class="sxs-lookup"><span data-stu-id="67d61-122">In this procedure we will add four lines to the BOM.</span></span> <span data-ttu-id="67d61-123">To linjer repræsenterer kabelindstillinger, og to linjer repræsenterer kabinetindstillinger.</span><span class="sxs-lookup"><span data-stu-id="67d61-123">Two lines represent cable options and two lines represent cabinet options.</span></span>  
1. <span data-ttu-id="67d61-124">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="67d61-124">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="67d61-125">Indtast eller vælg en værdi i feltet **Varenummer**.</span><span class="sxs-lookup"><span data-stu-id="67d61-125">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="67d61-126">Vælg varenummeret A0001, HDMI 6'-kabler.</span><span class="sxs-lookup"><span data-stu-id="67d61-126">Select item number A0001, HDMI 6' Cables.</span></span>  
1. <span data-ttu-id="67d61-127">Indtast eller vælg en værdi i feltet **Konfigurationsgruppe**.</span><span class="sxs-lookup"><span data-stu-id="67d61-127">In the **Configuration group** field, enter or select a value.</span></span>
    * <span data-ttu-id="67d61-128">Vælg den kabelkonfigurationsgruppe, der blev oprettet i vejledning 4 i denne sekvens.</span><span class="sxs-lookup"><span data-stu-id="67d61-128">Select the cable configuration group created in guide 4 in this sequence.</span></span>  
1. <span data-ttu-id="67d61-129">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="67d61-129">Select **New**.</span></span>
    * <span data-ttu-id="67d61-130">Vælg varenummeret A0002, HDMI 12'-kabler.</span><span class="sxs-lookup"><span data-stu-id="67d61-130">Select item number A0002, HDMI 12' Cables.</span></span>  
1. <span data-ttu-id="67d61-131">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="67d61-131">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="67d61-132">Indtast eller vælg en værdi i feltet **Varenummer**.</span><span class="sxs-lookup"><span data-stu-id="67d61-132">In the **Item number** field, enter or select a value.</span></span>
1. <span data-ttu-id="67d61-133">Indtast eller vælg en værdi i feltet **Konfigurationsgruppe**.</span><span class="sxs-lookup"><span data-stu-id="67d61-133">In the **Configuration group** field, enter or select a value.</span></span>
    * <span data-ttu-id="67d61-134">Vælg kabelkonfigurationsgruppen igen.</span><span class="sxs-lookup"><span data-stu-id="67d61-134">Select the cable configuration group again.</span></span>  
1. <span data-ttu-id="67d61-135">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="67d61-135">Select **New**.</span></span>
1. <span data-ttu-id="67d61-136">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="67d61-136">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="67d61-137">Indtast eller vælg en værdi i feltet **Varenummer**.</span><span class="sxs-lookup"><span data-stu-id="67d61-137">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="67d61-138">Vælg varenummeret D0002 Kabinet.</span><span class="sxs-lookup"><span data-stu-id="67d61-138">Select item number D0002 Cabinet.</span></span>  
1. <span data-ttu-id="67d61-139">Indtast eller vælg en værdi i feltet **Konfigurationsgruppe**.</span><span class="sxs-lookup"><span data-stu-id="67d61-139">In the **Configuration group** field, enter or select a value.</span></span>
    * <span data-ttu-id="67d61-140">Vælg kabinetkonfigurationsgruppen for denne styklistelinje.</span><span class="sxs-lookup"><span data-stu-id="67d61-140">Select the cabinet configuration group for this BOM line.</span></span>  
1. <span data-ttu-id="67d61-141">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="67d61-141">Select **New**.</span></span>
1. <span data-ttu-id="67d61-142">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="67d61-142">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="67d61-143">Indtast eller vælg en værdi i feltet **Varenummer**.</span><span class="sxs-lookup"><span data-stu-id="67d61-143">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="67d61-144">Vælg varenummeret M0007 Standardkabinet som den sidste styklistelinje.</span><span class="sxs-lookup"><span data-stu-id="67d61-144">Select Item number M0007 StandardCabinet as the last BOM line.</span></span>  
1. <span data-ttu-id="67d61-145">Indtast eller vælg en værdi i feltet **Konfigurationsgruppe**.</span><span class="sxs-lookup"><span data-stu-id="67d61-145">In the **Configuration group** field, enter or select a value.</span></span>
    * <span data-ttu-id="67d61-146">Vælg kabinetkonfigurationsgruppen for den sidste styklistelinje.</span><span class="sxs-lookup"><span data-stu-id="67d61-146">Select the Cabinet configuration group for the last BOM line.</span></span>  

## <a name="approve-and-activate"></a><span data-ttu-id="67d61-147">Godkend og aktivér</span><span class="sxs-lookup"><span data-stu-id="67d61-147">Approve and activate</span></span>

1. <span data-ttu-id="67d61-148">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="67d61-148">Close the page.</span></span>
1. <span data-ttu-id="67d61-149">Vælg **Godkend**.</span><span class="sxs-lookup"><span data-stu-id="67d61-149">Select **Approve**.</span></span>
1. <span data-ttu-id="67d61-150">Indtast eller vælg en værdi i feltet **Godkendt af**.</span><span class="sxs-lookup"><span data-stu-id="67d61-150">In the **Approved by** field, enter or select a value.</span></span>
1. <span data-ttu-id="67d61-151">Vælg *Ja* i feltet **Vil du også godkende styklisten?**.</span><span class="sxs-lookup"><span data-stu-id="67d61-151">Select *Yes* in the **Do you also want to approve the bill of materials?** field.</span></span>
1. <span data-ttu-id="67d61-152">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="67d61-152">Select **OK**.</span></span>
1. <span data-ttu-id="67d61-153">Vælg **Aktivér**.</span><span class="sxs-lookup"><span data-stu-id="67d61-153">Select **Activate**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]