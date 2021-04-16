---
title: Overføre fysisk lager på lagersted
description: Denne procedure fører dig gennem processen med at oprette og bogføre en lageroverførselskladde med henblik på at registrere flytning af en vare fra én lokalitet på et lagersted til en anden.
author: MarkusFogelberg
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a298f05185f3c81f2fde995e4d731b95a5f8d870
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832100"
---
# <a name="transfer-physical-inventory-within-the-warehouse"></a><span data-ttu-id="0908d-103">Overføre fysisk lager på lagersted</span><span class="sxs-lookup"><span data-stu-id="0908d-103">Transfer physical inventory within the warehouse</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0908d-104">Denne procedure fører dig gennem processen med at oprette og bogføre en lageroverførselskladde med henblik på at registrere flytning af en vare fra én lokalitet på et lagersted til en anden.</span><span class="sxs-lookup"><span data-stu-id="0908d-104">This procedure walks you through the process of creating and posting an inventory transfer journal in order to register movement of an item from one location in a warehouse to another.</span></span> <span data-ttu-id="0908d-105">Du skal have oprettet et lagerkladdenavn for lageroverførsler, før du begynder på dette.</span><span class="sxs-lookup"><span data-stu-id="0908d-105">You need to have an inventory journal name set up for inventory transfers before you start this.</span></span> <span data-ttu-id="0908d-106">Du kan gennemgå denne procedure i demodatafirmaet USMF ved hjælp af eksempel-værdierne, der vises, eller du kan bruge dine egne data, hvis du har konfigurerede produkter og lokaliteter.</span><span class="sxs-lookup"><span data-stu-id="0908d-106">You can walk through this procedure in demo data company USMF using the example values that are shown, or using you can use your own data if you have products and locations set up.</span></span> <span data-ttu-id="0908d-107">Disse opgaver udføres normalt af en lagermedarbejder.</span><span class="sxs-lookup"><span data-stu-id="0908d-107">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-transfer-journal"></a><span data-ttu-id="0908d-108">Oprette en lageroverførselskladde</span><span class="sxs-lookup"><span data-stu-id="0908d-108">Create an inventory transfer journal</span></span>
1. <span data-ttu-id="0908d-109">Gå i **Navigationsrude** til **Lagerstyring > Kladdeposter > Varer > Overfør**.</span><span class="sxs-lookup"><span data-stu-id="0908d-109">In the **Navigation pane**, go to **Inventory management > Journal entries > Items > Transfer**.</span></span>
2. <span data-ttu-id="0908d-110">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="0908d-110">Click **New**.</span></span>
3. <span data-ttu-id="0908d-111">Indtast eller vælg en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="0908d-111">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="0908d-112">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="0908d-112">Click **OK**.</span></span> <span data-ttu-id="0908d-113">Der er mulighed for at angive 'Fra' og 'Til'-dimensioner for hver kladdelinje.</span><span class="sxs-lookup"><span data-stu-id="0908d-113">There is the option to specify 'From' and 'To' dimensions for each journal line.</span></span> <span data-ttu-id="0908d-114">Disse er væsentlige for denne kladdetype.</span><span class="sxs-lookup"><span data-stu-id="0908d-114">These are essential for this journal type.</span></span> <span data-ttu-id="0908d-115">Du kan overflytte varer til lokalitet ved hjælp af forskellige regler.</span><span class="sxs-lookup"><span data-stu-id="0908d-115">You can transfer items to locations using different rules.</span></span> <span data-ttu-id="0908d-116">I dette eksempel vil vi overføre en vare inden for det samme lager fra en nummerpladestyret lokalitet til en lokalitet, der ikke er nummerpladestyret.</span><span class="sxs-lookup"><span data-stu-id="0908d-116">In this example we'll transfer an item within the same warehouse, from a license plate controlled location to a location that is not license plate controlled.</span></span>   

## <a name="create-journal-lines"></a><span data-ttu-id="0908d-117">Opret kladdelinjer</span><span class="sxs-lookup"><span data-stu-id="0908d-117">Create journal lines</span></span>
1. <span data-ttu-id="0908d-118">I **oversigtspanelet Kladdelinjer** skal du klikke på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="0908d-118">Int the **Journal lines fastTab**, click **New**.</span></span>
2. <span data-ttu-id="0908d-119">Indtast eller vælg en værdi i feltet **Varenummer**.</span><span class="sxs-lookup"><span data-stu-id="0908d-119">In the **Item number** field, enter or select a value.</span></span> <span data-ttu-id="0908d-120">Hvis du bruger USMF, kan du vælge 'A0001'.</span><span class="sxs-lookup"><span data-stu-id="0908d-120">If you are using USMF, you can select 'A0001'.</span></span>  
3. <span data-ttu-id="0908d-121">Indtast eller vælg en værdi i feltet **Fra sted**.</span><span class="sxs-lookup"><span data-stu-id="0908d-121">In the **From site** field, enter or select a value.</span></span> <span data-ttu-id="0908d-122">Hvis du bruger USMF, kan du vælge '2'.</span><span class="sxs-lookup"><span data-stu-id="0908d-122">If you are using USMF, you can select '2'.</span></span>  
4. <span data-ttu-id="0908d-123">Indtast eller vælg en værdi i feltet **Til sted**.</span><span class="sxs-lookup"><span data-stu-id="0908d-123">In the **To site** field, enter or select a value.</span></span> <span data-ttu-id="0908d-124">Hvis du bruger USMF, kan du vælge '2'.</span><span class="sxs-lookup"><span data-stu-id="0908d-124">If you are using USMF, you can select '2'.</span></span>  
5. <span data-ttu-id="0908d-125">Indtast eller vælg en værdi i feltet **Fra lagersted**.</span><span class="sxs-lookup"><span data-stu-id="0908d-125">In the **From warehouse** field, enter or select a value.</span></span> <span data-ttu-id="0908d-126">Hvis du bruger USMF, kan du vælge '24'.</span><span class="sxs-lookup"><span data-stu-id="0908d-126">If you are using USMF, you can select '24'.</span></span>  
6. <span data-ttu-id="0908d-127">Indtast eller vælg en værdi i feltet **Til lagersted**.</span><span class="sxs-lookup"><span data-stu-id="0908d-127">In the **To warehouse** field, enter or select a value.</span></span> <span data-ttu-id="0908d-128">Hvis du bruger USMF, kan du vælge '24'.</span><span class="sxs-lookup"><span data-stu-id="0908d-128">If you are using USMF, you can select '24'.</span></span>  
7. <span data-ttu-id="0908d-129">Indtast eller vælg en værdi i feltet **Fra lokalitet**.</span><span class="sxs-lookup"><span data-stu-id="0908d-129">In the **From location** field, enter or select a value.</span></span> <span data-ttu-id="0908d-130">Hvis du bruger USMF, kan du vælge 'FL-001'.</span><span class="sxs-lookup"><span data-stu-id="0908d-130">If you are using USMF, you can select 'FL-001'.</span></span>  
8. <span data-ttu-id="0908d-131">Indtast eller vælg en værdi i feltet **Til lokalitet**.</span><span class="sxs-lookup"><span data-stu-id="0908d-131">In the **To location** field, enter or select a value.</span></span> <span data-ttu-id="0908d-132">Hvis du bruger USMF, kan du vælge 'BULK-001'.</span><span class="sxs-lookup"><span data-stu-id="0908d-132">If you are using USMF, you can select 'BULK-001'.</span></span>  
9. <span data-ttu-id="0908d-133">Angiv et tal i feltet **Antal**.</span><span class="sxs-lookup"><span data-stu-id="0908d-133">In the **Quantity** field, enter a number.</span></span>
10. <span data-ttu-id="0908d-134">Klik på fanen **Lagerdimensioner** i oversigtspanelet **Linjedetaljer**.</span><span class="sxs-lookup"><span data-stu-id="0908d-134">In the **Line details** fastTab, click the **Inventory dimensions** tab.</span></span>
11. <span data-ttu-id="0908d-135">I **Fra lagerdimensioner** skal du angive eller vælge en værdi i feltet **Id-nummer**.</span><span class="sxs-lookup"><span data-stu-id="0908d-135">In **From inventory dimensions**, in the **License plate** field, enter or select a value.</span></span> <span data-ttu-id="0908d-136">Hvis du bruger USMF, kan du vælge '24'.</span><span class="sxs-lookup"><span data-stu-id="0908d-136">If you are using USMF, you can select '24'.</span></span>  
12. <span data-ttu-id="0908d-137">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="0908d-137">Click **Save**.</span></span>

## <a name="post-the-inventory-transfer-journal"></a><span data-ttu-id="0908d-138">Bogfør lageroverførselskladden</span><span class="sxs-lookup"><span data-stu-id="0908d-138">Post the inventory transfer journal</span></span>
1. <span data-ttu-id="0908d-139">Klik på **Bogfør** i **handlingsruden**.</span><span class="sxs-lookup"><span data-stu-id="0908d-139">On the **Action Pane**, click **Post**.</span></span>
2. <span data-ttu-id="0908d-140">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="0908d-140">Click **OK**.</span></span>

## <a name="view-inventory-transactions"></a><span data-ttu-id="0908d-141">Få vist lagertransaktioner</span><span class="sxs-lookup"><span data-stu-id="0908d-141">View inventory transactions</span></span>
1. <span data-ttu-id="0908d-142">Klik på **Lager**.</span><span class="sxs-lookup"><span data-stu-id="0908d-142">Click **Inventory**.</span></span>
2. <span data-ttu-id="0908d-143">Klik på **Transaktioner**.</span><span class="sxs-lookup"><span data-stu-id="0908d-143">Click **Transactions**.</span></span> <span data-ttu-id="0908d-144">Her kan du se de posteringer, der blev oprettet, da du bogførte kladden.</span><span class="sxs-lookup"><span data-stu-id="0908d-144">Here you can see the transactions that were created when you posted your journal.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]