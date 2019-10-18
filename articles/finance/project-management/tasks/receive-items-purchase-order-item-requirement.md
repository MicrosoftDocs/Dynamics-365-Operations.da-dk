---
title: Modtage varer på indkøbsordre ud fra varebehov
description: I dette emne beskrives, hvordan du modtager varer i en indkøbsordre fra et varebehov.
author: KimANelson
manager: AnnBe
ms.date: 08/06/2019
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
ms.openlocfilehash: 7afdae65c5ae7e3196c6b9f142dd87aec39b5ea3
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174414"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="bf1b9-103">Modtage varer på indkøbsordre ud fra varebehov</span><span class="sxs-lookup"><span data-stu-id="bf1b9-103">Receive items on purchase order from item requirement</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bf1b9-104">I dette emne beskrives, hvordan du modtager varer i en indkøbsordre fra et varebehov.</span><span class="sxs-lookup"><span data-stu-id="bf1b9-104">This topic explains how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="bf1b9-105">Når du bruger et varebehov i stedet for en varepostering, kan du planlægge leveringen, så den finder sted, umiddelbart før varen faktisk skal bruges. Du kan oprette en indkøbsordre, lade varen indgå i samhandelsaftaler og lade varebehovet indgå i produktionsplanlægningen.</span><span class="sxs-lookup"><span data-stu-id="bf1b9-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="bf1b9-106">Denne opgave bruger USSI-datasættet.</span><span class="sxs-lookup"><span data-stu-id="bf1b9-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="bf1b9-107">Gå i navigationsruden til **Moduler > Projektstyring og regnskab > Projekter > Alle projekter**.</span><span class="sxs-lookup"><span data-stu-id="bf1b9-107">In the navigation pane, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="bf1b9-108">Vælg linket i den ønskede række på listen.</span><span class="sxs-lookup"><span data-stu-id="bf1b9-108">In the list, select the link in the desired row.</span></span>
3. <span data-ttu-id="bf1b9-109">Vælg **Plan** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="bf1b9-109">On the Action Pane, select **Plan**.</span></span>
4. <span data-ttu-id="bf1b9-110">Vælg **Varebehov**.</span><span class="sxs-lookup"><span data-stu-id="bf1b9-110">Select **Item requirements**.</span></span>
5. <span data-ttu-id="bf1b9-111">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="bf1b9-111">Select **New**.</span></span>
6. <span data-ttu-id="bf1b9-112">Indtast eller vælg en værdi i feltet **Varenummer** i den nye række.</span><span class="sxs-lookup"><span data-stu-id="bf1b9-112">In the new row, enter or select a value in the **Item number** field.</span></span>
7. <span data-ttu-id="bf1b9-113">Angiv et tal i feltet **Antal**.</span><span class="sxs-lookup"><span data-stu-id="bf1b9-113">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="bf1b9-114">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="bf1b9-114">Select **Save**.</span></span>
9. <span data-ttu-id="bf1b9-115">Vælg **Administrer** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="bf1b9-115">On the Action Pane, select **Manage**.</span></span>
10. <span data-ttu-id="bf1b9-116">Vælg **Funktioner**.</span><span class="sxs-lookup"><span data-stu-id="bf1b9-116">Select **Functions**.</span></span>
11. <span data-ttu-id="bf1b9-117">Vælg **Opret indkøbsordre**.</span><span class="sxs-lookup"><span data-stu-id="bf1b9-117">Select **Create purchase order**.</span></span>
12. <span data-ttu-id="bf1b9-118">Marker afkrydsningsfeltet **Medtag alle**.</span><span class="sxs-lookup"><span data-stu-id="bf1b9-118">Select the **Include all** check box.</span></span>
13. <span data-ttu-id="bf1b9-119">Indtast eller vælg en værdi i feltet **Kreditorkonto**.</span><span class="sxs-lookup"><span data-stu-id="bf1b9-119">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="bf1b9-120">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="bf1b9-120">Select **OK**.</span></span>
15. <span data-ttu-id="bf1b9-121">I navigationsruden skal du gå til **Moduler > Kreditor > Indkøbsordrer > Alle indkøbsordrer**.</span><span class="sxs-lookup"><span data-stu-id="bf1b9-121">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > All purchase orders**.</span></span>
16. <span data-ttu-id="bf1b9-122">Vælg linket i den ønskede række på listen.</span><span class="sxs-lookup"><span data-stu-id="bf1b9-122">In the list, select the link in the desired row.</span></span>
17. <span data-ttu-id="bf1b9-123">Klik på **Køb** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="bf1b9-123">On the Action Pane, select **Purchase**.</span></span>
18. <span data-ttu-id="bf1b9-124">Vælg **Bekræft**.</span><span class="sxs-lookup"><span data-stu-id="bf1b9-124">Select **Confirm**.</span></span>
19. <span data-ttu-id="bf1b9-125">Vælg **Modtag** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="bf1b9-125">On the Action Pane, select **Receive**.</span></span>
20. <span data-ttu-id="bf1b9-126">Vælg **Produktkvittering**.</span><span class="sxs-lookup"><span data-stu-id="bf1b9-126">Select **Product receipt**.</span></span>
21. <span data-ttu-id="bf1b9-127">Skriv en værdi i feltet **Produktkvittering**.</span><span class="sxs-lookup"><span data-stu-id="bf1b9-127">In the **Product receipt** field, type a value.</span></span>
22. <span data-ttu-id="bf1b9-128">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="bf1b9-128">Select **OK**.</span></span>

