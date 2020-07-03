---
title: Registrere modtagelsen af varer for indkøbsordren
description: Dette emne beskriver, hvordan du registrerer modtagelsen af varer direkte på en indkøbsordre.
author: mkirknel
manager: tfehr
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1aa4043aca2e53eae32256a98d556c25b4ec1957
ms.sourcegitcommit: ac47e8679fb104515f7dcca509294264bd05d2b1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/15/2020
ms.locfileid: "3454781"
---
# <a name="record-the-receipt-of-goods-on-the-purchase-order"></a><span data-ttu-id="e6d53-103">Registrere modtagelsen af varer for indkøbsordren</span><span class="sxs-lookup"><span data-stu-id="e6d53-103">Record the receipt of goods on the purchase order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e6d53-104">Dette emne beskriver, hvordan du registrerer modtagelsen af varer direkte på en indkøbsordre.</span><span class="sxs-lookup"><span data-stu-id="e6d53-104">This topic explains how to record receipt of goods directly on a purchase order.</span></span> <span data-ttu-id="e6d53-105">Du kan også registrere produktkvitteringen på lagerstedet og derefter bogføre det senere på indkøbsordren.</span><span class="sxs-lookup"><span data-stu-id="e6d53-105">It's also possible to register product receipt in the warehouse, and then later record it on the purchase order.</span></span> <span data-ttu-id="e6d53-106">Denne opgave udføres typisk af en indkøber eller en kreditorkoordinator.</span><span class="sxs-lookup"><span data-stu-id="e6d53-106">This task is typically done by a purchasing agent or an accounts payable coordinator.</span></span> <span data-ttu-id="e6d53-107">Eksemplet i denne vejledning kan bruges i demodatafirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="e6d53-107">The example shown in this guide can be used in the USMF demo data company.</span></span> <span data-ttu-id="e6d53-108">Eksemplet indeholder trin til oprettelse af en enkelt indkøbsordre, så du kan afspille proceduren som en opgave.</span><span class="sxs-lookup"><span data-stu-id="e6d53-108">The example includes steps to create a simple purchase order so that you can play the procedure as a task guide.</span></span> <span data-ttu-id="e6d53-109">Hvis du har brugt proceduren for dine egne data, skal du starte med underopgaven **Registrer modtagelsen af varer**.</span><span class="sxs-lookup"><span data-stu-id="e6d53-109">If you were using the procedure on your own data, you would start at the **Record receipt of goods** subtask.</span></span>


## <a name="prepare-a-new-purchase-order-for-receipt-of-goods"></a><span data-ttu-id="e6d53-110">Udarbejd en ny indkøbsordre for modtagelsen af varer</span><span class="sxs-lookup"><span data-stu-id="e6d53-110">Prepare a new purchase order for receipt of goods</span></span>
1. <span data-ttu-id="e6d53-111">Gå til **Navigationsruden > Moduler > Indkøb og forsyning > Indkøbsordrer > Alle indkøbsordrer**.</span><span class="sxs-lookup"><span data-stu-id="e6d53-111">Go to **Navigation pane > Modules > Procurement and sourcing > Purchase orders > All purchase orders**.</span></span>
2. <span data-ttu-id="e6d53-112">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="e6d53-112">Select **New**.</span></span>
3. <span data-ttu-id="e6d53-113">I feltet **Leverandørkonto** skal du indtaste `US-101`.</span><span class="sxs-lookup"><span data-stu-id="e6d53-113">In the **Vendor account** field, enter `US-101`.</span></span>
4. <span data-ttu-id="e6d53-114">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="e6d53-114">Select **OK**.</span></span>
5. <span data-ttu-id="e6d53-115">I feltet **Varenummer** skal du indtaste `M0001`.</span><span class="sxs-lookup"><span data-stu-id="e6d53-115">In the **Item number** field, enter `M0001`.</span></span>
6. <span data-ttu-id="e6d53-116">I feltet **Antal** skal du indtaste `5`.</span><span class="sxs-lookup"><span data-stu-id="e6d53-116">In the **Quantity** field, enter `5`.</span></span>
7. <span data-ttu-id="e6d53-117">Klik på **Køb** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="e6d53-117">On the Action Pane, select **Purchase**.</span></span>
8. <span data-ttu-id="e6d53-118">Vælg **Bekræft**.</span><span class="sxs-lookup"><span data-stu-id="e6d53-118">Select **Confirm**.</span></span>

## <a name="record-receipt-of-goods"></a><span data-ttu-id="e6d53-119">Postér modtagelse af varer</span><span class="sxs-lookup"><span data-stu-id="e6d53-119">Record receipt of goods</span></span>
1. <span data-ttu-id="e6d53-120">Vælg **Modtag** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="e6d53-120">On the Action Pane, select **Receive**.</span></span>
2. <span data-ttu-id="e6d53-121">Vælg **Produktkvittering**.</span><span class="sxs-lookup"><span data-stu-id="e6d53-121">Select **Product receipt**.</span></span> <span data-ttu-id="e6d53-122">I feltet **Antal** kan du vælge forskellige indstillinger for det antal, du vil modtage.</span><span class="sxs-lookup"><span data-stu-id="e6d53-122">The **Quantity** field allows you to select different options for the quantity that you want to receive.</span></span> <span data-ttu-id="e6d53-123">Hvis der f.eks. tidligere er registreret et antal på lageret, kan du vælge **Registreret antal**.</span><span class="sxs-lookup"><span data-stu-id="e6d53-123">For example, if a quantity has previously been registered in the warehouse, you can select **Registered quantity**.</span></span> <span data-ttu-id="e6d53-124">I dette eksempel kan du bruge værdien **Bestilt antal**.</span><span class="sxs-lookup"><span data-stu-id="e6d53-124">For this example, use the value **Ordered quantity**.</span></span>
3. <span data-ttu-id="e6d53-125">Udvid sektionen **Oversigt**.</span><span class="sxs-lookup"><span data-stu-id="e6d53-125">Expand the **Overview** section.</span></span>
4. <span data-ttu-id="e6d53-126">Skriv en hvilken som helst værdi i feltet **Produktkvittering**.</span><span class="sxs-lookup"><span data-stu-id="e6d53-126">In the **Product receipt** field, type any value.</span></span> <span data-ttu-id="e6d53-127">Dette felt bruges til at angive en reference, der skal bruges som bilag for produktkvitteringskladden.</span><span class="sxs-lookup"><span data-stu-id="e6d53-127">This field is used to enter a reference that will be used as voucher for the product receipt journal.</span></span>  
5. <span data-ttu-id="e6d53-128">Udvid sektionen **Linjer**.</span><span class="sxs-lookup"><span data-stu-id="e6d53-128">Expand the **Lines** section.</span></span>
6. <span data-ttu-id="e6d53-129">Angiv **Antal** til '4'.</span><span class="sxs-lookup"><span data-stu-id="e6d53-129">Set **Quantity** to '4'.</span></span> <span data-ttu-id="e6d53-130">Her kan du manuelt angive det antal, der modtages for hver linje på ordren.</span><span class="sxs-lookup"><span data-stu-id="e6d53-130">Here you are able to manually specify the quantity that is being received for each line on the order.</span></span>  
7. <span data-ttu-id="e6d53-131">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="e6d53-131">Select **OK**.</span></span> <span data-ttu-id="e6d53-132">Varerne er nu registreret som modtaget på indkøbsordren, og der er oprettet en produktkvitteringskladde som dokument for at afspejle dette.</span><span class="sxs-lookup"><span data-stu-id="e6d53-132">The goods have now been recorded as received on the purchase order, and a product receipt journal has been created as document to reflect this.</span></span> <span data-ttu-id="e6d53-133">Du kan bruge handlingen Produktkvittering til at gennemse de kladder, der er oprettet med indkøbsordren, og til at se, hvad der er modtaget, og hvornår.</span><span class="sxs-lookup"><span data-stu-id="e6d53-133">You can use the Product receipt action to review the journals created with the purchase order, and see what was received, and when.</span></span>  

