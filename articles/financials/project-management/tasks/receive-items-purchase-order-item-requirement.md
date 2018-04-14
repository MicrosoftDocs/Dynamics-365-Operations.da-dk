--- 
title: "Modtage varer på indkøbsordre ud fra varebehov"
description: "Denne procedure viser, hvordan du modtager varer på en købsordre fra et varebehov."
author: KimANelson
manager: AnnBe
ms.date: 02/13/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: fef6a597ed126ff4e1148fd9710b214c0425c3ab
ms.contentlocale: da-dk
ms.lasthandoff: 04/13/2018

---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="accb0-103">Modtage varer på indkøbsordre ud fra varebehov</span><span class="sxs-lookup"><span data-stu-id="accb0-103">Receive items on purchase order from item requirement</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="accb0-104">Denne procedure viser, hvordan du modtager varer på en købsordre fra et varebehov.</span><span class="sxs-lookup"><span data-stu-id="accb0-104">This procedure shows how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="accb0-105">Når du bruger et varebehov i stedet for en varepostering, kan du planlægge leveringen, så den finder sted, umiddelbart før varen faktisk skal bruges. Du kan oprette en indkøbsordre, lade varen indgå i samhandelsaftaler og lade varebehovet indgå i produktionsplanlægningen.</span><span class="sxs-lookup"><span data-stu-id="accb0-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="accb0-106">Denne opgave bruger USSI-datasættet.</span><span class="sxs-lookup"><span data-stu-id="accb0-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="accb0-107">Gå til Projektstyring og regnskab > Projekter > Alle projekter.</span><span class="sxs-lookup"><span data-stu-id="accb0-107">Go to Project management and accounting > Projects > All projects.</span></span>
2. <span data-ttu-id="accb0-108">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="accb0-108">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="accb0-109">Klik på Plan i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="accb0-109">On the Action Pane, click Plan.</span></span>
4. <span data-ttu-id="accb0-110">Klik på Varebehov.</span><span class="sxs-lookup"><span data-stu-id="accb0-110">Click Item requirements.</span></span>
5. <span data-ttu-id="accb0-111">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="accb0-111">Click New.</span></span>
6. <span data-ttu-id="accb0-112">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="accb0-112">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="accb0-113">Indtast eller vælg en værdi i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="accb0-113">In the Item number field, enter or select a value.</span></span>
8. <span data-ttu-id="accb0-114">Angiv et tal i feltet Antal.</span><span class="sxs-lookup"><span data-stu-id="accb0-114">In the Quantity field, enter a number.</span></span>
9. <span data-ttu-id="accb0-115">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="accb0-115">Click Save.</span></span>
10. <span data-ttu-id="accb0-116">Klik på Administrer i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="accb0-116">On the Action Pane, click Manage.</span></span>
11. <span data-ttu-id="accb0-117">Klik på Funktioner.</span><span class="sxs-lookup"><span data-stu-id="accb0-117">Click Functions.</span></span>
12. <span data-ttu-id="accb0-118">Klik på Opret indkøbsordre automatisk.</span><span class="sxs-lookup"><span data-stu-id="accb0-118">Click Create purchase order.</span></span>
13. <span data-ttu-id="accb0-119">Marker afkrydsningsfeltet Medtag.</span><span class="sxs-lookup"><span data-stu-id="accb0-119">Select the Include check box.</span></span>
14. <span data-ttu-id="accb0-120">Indtast eller vælg en værdi i feltet Kreditorkonto.</span><span class="sxs-lookup"><span data-stu-id="accb0-120">In the Vendor account field, enter or select a value.</span></span>
15. <span data-ttu-id="accb0-121">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="accb0-121">Click OK.</span></span>
16. <span data-ttu-id="accb0-122">Gå til Kreditor > Indkøbsordrer > Alle indkøbsordrer.</span><span class="sxs-lookup"><span data-stu-id="accb0-122">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
17. <span data-ttu-id="accb0-123">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="accb0-123">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="accb0-124">Klik på Køb i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="accb0-124">On the Action Pane, click Purchase.</span></span>
19. <span data-ttu-id="accb0-125">Klik på Bekræft.</span><span class="sxs-lookup"><span data-stu-id="accb0-125">Click Confirm.</span></span>
20. <span data-ttu-id="accb0-126">Klik på Modtag i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="accb0-126">On the Action Pane, click Receive.</span></span>
21. <span data-ttu-id="accb0-127">Klik på Produktkvittering.</span><span class="sxs-lookup"><span data-stu-id="accb0-127">Click Product receipt.</span></span>
22. <span data-ttu-id="accb0-128">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="accb0-128">In the list, mark the selected row.</span></span>
23. <span data-ttu-id="accb0-129">Skriv en værdi i feltet Produktkvittering.</span><span class="sxs-lookup"><span data-stu-id="accb0-129">In the Product receipt field, type a value.</span></span>
24. <span data-ttu-id="accb0-130">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="accb0-130">Click OK.</span></span>


