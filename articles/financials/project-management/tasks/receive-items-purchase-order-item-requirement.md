---
title: Modtage varer på indkøbsordre ud fra varebehov
description: Denne procedure viser, hvordan du modtager varer på en købsordre fra et varebehov.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fee2c965b0c065f00564b849ec93504336fb3f60
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838241"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="116b4-103">Modtage varer på indkøbsordre ud fra varebehov</span><span class="sxs-lookup"><span data-stu-id="116b4-103">Receive items on purchase order from item requirement</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="116b4-104">Denne procedure viser, hvordan du modtager varer på en købsordre fra et varebehov.</span><span class="sxs-lookup"><span data-stu-id="116b4-104">This procedure shows how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="116b4-105">Når du bruger et varebehov i stedet for en varepostering, kan du planlægge leveringen, så den finder sted, umiddelbart før varen faktisk skal bruges. Du kan oprette en indkøbsordre, lade varen indgå i samhandelsaftaler og lade varebehovet indgå i produktionsplanlægningen.</span><span class="sxs-lookup"><span data-stu-id="116b4-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="116b4-106">Denne opgave bruger USSI-datasættet.</span><span class="sxs-lookup"><span data-stu-id="116b4-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="116b4-107">Gå til Projektstyring og regnskab > Projekter > Alle projekter.</span><span class="sxs-lookup"><span data-stu-id="116b4-107">Go to Project management and accounting > Projects > All projects.</span></span>
2. <span data-ttu-id="116b4-108">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="116b4-108">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="116b4-109">Klik på Plan i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="116b4-109">On the Action Pane, click Plan.</span></span>
4. <span data-ttu-id="116b4-110">Klik på Varebehov.</span><span class="sxs-lookup"><span data-stu-id="116b4-110">Click Item requirements.</span></span>
5. <span data-ttu-id="116b4-111">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="116b4-111">Click New.</span></span>
6. <span data-ttu-id="116b4-112">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="116b4-112">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="116b4-113">Indtast eller vælg en værdi i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="116b4-113">In the Item number field, enter or select a value.</span></span>
8. <span data-ttu-id="116b4-114">Angiv et tal i feltet Antal.</span><span class="sxs-lookup"><span data-stu-id="116b4-114">In the Quantity field, enter a number.</span></span>
9. <span data-ttu-id="116b4-115">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="116b4-115">Click Save.</span></span>
10. <span data-ttu-id="116b4-116">Klik på Administrer i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="116b4-116">On the Action Pane, click Manage.</span></span>
11. <span data-ttu-id="116b4-117">Klik på Funktioner.</span><span class="sxs-lookup"><span data-stu-id="116b4-117">Click Functions.</span></span>
12. <span data-ttu-id="116b4-118">Klik på Opret indkøbsordre automatisk.</span><span class="sxs-lookup"><span data-stu-id="116b4-118">Click Create purchase order.</span></span>
13. <span data-ttu-id="116b4-119">Marker afkrydsningsfeltet Medtag.</span><span class="sxs-lookup"><span data-stu-id="116b4-119">Select the Include check box.</span></span>
14. <span data-ttu-id="116b4-120">Indtast eller vælg en værdi i feltet Kreditorkonto.</span><span class="sxs-lookup"><span data-stu-id="116b4-120">In the Vendor account field, enter or select a value.</span></span>
15. <span data-ttu-id="116b4-121">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="116b4-121">Click OK.</span></span>
16. <span data-ttu-id="116b4-122">Gå til Kreditor > Indkøbsordrer > Alle indkøbsordrer.</span><span class="sxs-lookup"><span data-stu-id="116b4-122">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
17. <span data-ttu-id="116b4-123">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="116b4-123">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="116b4-124">Klik på Køb i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="116b4-124">On the Action Pane, click Purchase.</span></span>
19. <span data-ttu-id="116b4-125">Klik på Bekræft.</span><span class="sxs-lookup"><span data-stu-id="116b4-125">Click Confirm.</span></span>
20. <span data-ttu-id="116b4-126">Klik på Modtag i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="116b4-126">On the Action Pane, click Receive.</span></span>
21. <span data-ttu-id="116b4-127">Klik på Produktkvittering.</span><span class="sxs-lookup"><span data-stu-id="116b4-127">Click Product receipt.</span></span>
22. <span data-ttu-id="116b4-128">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="116b4-128">In the list, mark the selected row.</span></span>
23. <span data-ttu-id="116b4-129">Skriv en værdi i feltet Produktkvittering.</span><span class="sxs-lookup"><span data-stu-id="116b4-129">In the Product receipt field, type a value.</span></span>
24. <span data-ttu-id="116b4-130">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="116b4-130">Click OK.</span></span>

