--- 
title: "Registrere modtagelsen af varer for indkøbsordren"
description: "Denne fremgangsmåde viser, hvordan du registrerer modtagelsen af varer direkte på en indkøbsordre."
author: FrankDahl
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 3a9c87b8790ed6cfe4139180f1f1785db04e7431
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---
# <a name="record-the-receipt-of-goods-on-the-purchase-order"></a><span data-ttu-id="f7d22-103">Registrere modtagelsen af varer for indkøbsordren</span><span class="sxs-lookup"><span data-stu-id="f7d22-103">Record the receipt of goods on the purchase order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f7d22-104">Denne fremgangsmåde viser, hvordan du registrerer modtagelsen af varer direkte på en indkøbsordre.</span><span class="sxs-lookup"><span data-stu-id="f7d22-104">This procedure shows you how to record receipt of goods directly on a purchase order.</span></span> <span data-ttu-id="f7d22-105">Du kan også registrere produktkvitteringen på lagerstedet og derefter bogføre det senere på indkøbsordren.</span><span class="sxs-lookup"><span data-stu-id="f7d22-105">It’s also possible to register product receipt in the warehouse, and then later record it on the purchase order.</span></span> <span data-ttu-id="f7d22-106">Denne opgave udføres typisk af en indkøber eller en kreditorkoordinator.</span><span class="sxs-lookup"><span data-stu-id="f7d22-106">This task is typically done by a purchasing agent or an accounts payable coordinator.</span></span> <span data-ttu-id="f7d22-107">Eksemplet i denne vejledning kan bruges i demodatafirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="f7d22-107">The example shown in this guide can be used in the USMF demo data company.</span></span> <span data-ttu-id="f7d22-108">Eksemplet indeholder trin til oprettelse af en enkelt indkøbsordre, så du kan afspille proceduren som en opgave.</span><span class="sxs-lookup"><span data-stu-id="f7d22-108">The example includes steps to create a simple purchase order so that you can play the procedure as a task guide.</span></span> <span data-ttu-id="f7d22-109">Hvis du bruger fremgangsmåden på dine egne data, skal du starte med underopgaven for postering af modtagelsen af varerne.</span><span class="sxs-lookup"><span data-stu-id="f7d22-109">If you were using the procedure on your own data, you would start at the Record receipt of goods subtask.</span></span>


## <a name="prepare-a-new-purchase-order-for-receipt-of-goods"></a><span data-ttu-id="f7d22-110">Udarbejd en ny indkøbsordre for modtagelsen af varer</span><span class="sxs-lookup"><span data-stu-id="f7d22-110">Prepare a new purchase order for receipt of goods</span></span>
1. <span data-ttu-id="f7d22-111">Gå til Indkøb og forsyning > Indkøbsordrer > Alle indkøbsordrer.</span><span class="sxs-lookup"><span data-stu-id="f7d22-111">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="f7d22-112">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="f7d22-112">Click New.</span></span>
3. <span data-ttu-id="f7d22-113">Skriv "US-101" i feltet Kreditorkonto.</span><span class="sxs-lookup"><span data-stu-id="f7d22-113">In the Vendor account field, enter US-101.</span></span>
4. <span data-ttu-id="f7d22-114">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="f7d22-114">Click OK.</span></span>
5. <span data-ttu-id="f7d22-115">Indtast M0001 i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="f7d22-115">In the Item number field, enter M0001.</span></span>
6. <span data-ttu-id="f7d22-116">Skriv 5 i feltet Antal.</span><span class="sxs-lookup"><span data-stu-id="f7d22-116">In the Quantity field, enter 5.</span></span>
7. <span data-ttu-id="f7d22-117">Klik på Køb i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="f7d22-117">On the Action Pane, click Purchase.</span></span>
8. <span data-ttu-id="f7d22-118">Klik på Bekræft.</span><span class="sxs-lookup"><span data-stu-id="f7d22-118">Click Confirm.</span></span>

## <a name="record-receipt-of-goods"></a><span data-ttu-id="f7d22-119">Postér modtagelse af varer</span><span class="sxs-lookup"><span data-stu-id="f7d22-119">Record receipt of goods</span></span>
1. <span data-ttu-id="f7d22-120">Klik på Modtag i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="f7d22-120">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="f7d22-121">Klik på Produktkvittering.</span><span class="sxs-lookup"><span data-stu-id="f7d22-121">Click Product receipt.</span></span>
    * <span data-ttu-id="f7d22-122">I feltet Antal kan du vælge forskellige indstillinger for det antal, du vil modtage.</span><span class="sxs-lookup"><span data-stu-id="f7d22-122">The Quantity field allows you to select different options for the quantity that you want to receive.</span></span> <span data-ttu-id="f7d22-123">Hvis der f.eks. tidligere er registreret et antal på lageret, kan du vælge Registreret antal.</span><span class="sxs-lookup"><span data-stu-id="f7d22-123">For example, if a quantity has previously been registered in the warehouse, you can select Registered quantity.</span></span>  <span data-ttu-id="f7d22-124">I dette eksempel kan du bruge værdien i Bestilt antal.</span><span class="sxs-lookup"><span data-stu-id="f7d22-124">For this example, use the value Ordered quantity.</span></span>   
3. <span data-ttu-id="f7d22-125">Skriv en hvilken som helst værdi i feltet Produktkvittering.</span><span class="sxs-lookup"><span data-stu-id="f7d22-125">In the Product receipt field, type any value.</span></span>
    * <span data-ttu-id="f7d22-126">Dette felt bruges til at angive en reference, der skal bruges som bilag for produktkvitteringskladden.</span><span class="sxs-lookup"><span data-stu-id="f7d22-126">This field is used to enter a reference that will be used as voucher for the product receipt journal.</span></span>  
4. <span data-ttu-id="f7d22-127">Udvid sektionen Linjer.</span><span class="sxs-lookup"><span data-stu-id="f7d22-127">Expand the Lines section.</span></span>
5. <span data-ttu-id="f7d22-128">Angiv antallet til '4'.</span><span class="sxs-lookup"><span data-stu-id="f7d22-128">Set Quantity to '4'.</span></span>
    * <span data-ttu-id="f7d22-129">Her kan du manuelt angive det antal, der modtages for hver linje på ordren.</span><span class="sxs-lookup"><span data-stu-id="f7d22-129">Here you are able to manually specify the quantity that is being received for each line on the order.</span></span>  
6. <span data-ttu-id="f7d22-130">Skjul sektionen Linjer.</span><span class="sxs-lookup"><span data-stu-id="f7d22-130">Collapse the Lines section.</span></span>
7. <span data-ttu-id="f7d22-131">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="f7d22-131">Click OK.</span></span>
    * <span data-ttu-id="f7d22-132">Varerne er nu registreret som modtaget på indkøbsordren, og der er oprettet en produktkvitteringskladde som dokument for at afspejle dette.</span><span class="sxs-lookup"><span data-stu-id="f7d22-132">The goods have now been recorded as received on the purchase order, and a product receipt journal has been created as document to reflect this.</span></span> <span data-ttu-id="f7d22-133">Du kan bruge handlingen Produktkvittering til at gennemse de kladder, der er oprettet med indkøbsordren, og til at se, hvad der er modtaget, og hvornår.</span><span class="sxs-lookup"><span data-stu-id="f7d22-133">You can use the Product receipt action to review the journals created with the purchase order, and see what was received, and when.</span></span>  


