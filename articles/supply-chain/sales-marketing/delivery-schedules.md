---
title: Leveranceplaner
description: "Leveranceplaner giver dig mulighed for at spore antallet, når du bruger flere leverancer til en enkelt salgsordre, et salgstilbud eller en indkøbsordre."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchDeliverySchedule, SalesDeliverySchedule, SalesQuotationDeliverySchedule
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 213984
ms.assetid: 44cac104-c36c-4371-a992-9178b3fd65e9
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 84ae84a567e5f45bc0b20538d04917c6feb21336
ms.contentlocale: da-dk
ms.lasthandoff: 07/18/2017

---

# <a name="delivery-schedules"></a><span data-ttu-id="54491-103">Leveranceplaner</span><span class="sxs-lookup"><span data-stu-id="54491-103">Delivery schedules</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="54491-104">Leveranceplaner giver dig mulighed for at spore antallet, når du bruger flere leverancer til en enkelt salgsordre, et salgstilbud eller en indkøbsordre.</span><span class="sxs-lookup"><span data-stu-id="54491-104">Delivery schedules allow you to track order line quantity when you are using multiple deliveries for a single sales order, sales quotation, or purchase order.</span></span>

<span data-ttu-id="54491-105">Brug en leveranceplan bruges, når det samlede antal i en ordre eller et tilbud skal leveres i flere leverancer.</span><span class="sxs-lookup"><span data-stu-id="54491-105">Use a delivery schedule when the total quantity on an order or quotation line must be delivered in multiple shipments.</span></span> <span data-ttu-id="54491-106">Individuelle leverancer repræsenteres af leveringslinjer.</span><span class="sxs-lookup"><span data-stu-id="54491-106">Individual shipments are represented by delivery lines.</span></span> <span data-ttu-id="54491-107">To eller flere leverancelinjer udgør én leveranceplan.</span><span class="sxs-lookup"><span data-stu-id="54491-107">Two or more delivery lines make up one delivery schedule.</span></span> <span data-ttu-id="54491-108">Leverancelinjerne kan have forskellige leveringsdatoer, antal, leveringsmåder og lagringsdimensioner, som f.eks. sted og lagersted.</span><span class="sxs-lookup"><span data-stu-id="54491-108">The delivery lines can have different delivery dates, quantities, modes of delivery, and storage dimensions, such as site and warehouse.</span></span>  

<span data-ttu-id="54491-109">**Eksempel på en leveranceplan**</span><span class="sxs-lookup"><span data-stu-id="54491-109">**Example of a delivery schedule**</span></span>

|                                   |                                          |
|-----------------------------------|------------------------------------------|
| <span data-ttu-id="54491-110">Samlet ordre (oprindelig salgsordrelinje)</span><span class="sxs-lookup"><span data-stu-id="54491-110">Total order (original order line)</span></span> | <span data-ttu-id="54491-111">600 stole</span><span class="sxs-lookup"><span data-stu-id="54491-111">600 chairs</span></span>                               |
| <span data-ttu-id="54491-112">Ønsket leveranceplan</span><span class="sxs-lookup"><span data-stu-id="54491-112">Requested delivery schedule</span></span>       | <span data-ttu-id="54491-113">100 stole pr. måned</span><span class="sxs-lookup"><span data-stu-id="54491-113">100 chairs per month</span></span>                     |
| <span data-ttu-id="54491-114">Ønsket tidsramme for leverance</span><span class="sxs-lookup"><span data-stu-id="54491-114">Requested time frame for delivery</span></span> | <span data-ttu-id="54491-115">6 måneder, på den første dag i hver måned</span><span class="sxs-lookup"><span data-stu-id="54491-115">6 months, on the first day of each month</span></span> |

<span data-ttu-id="54491-116">I dette scenario anmoder kunden om en leverance på 600 stole i batch på 100 stole over en periode på seks måneder.</span><span class="sxs-lookup"><span data-stu-id="54491-116">In this scenario, the customer requests delivery of 600 chairs in batches of 100 chairs over a period of six months.</span></span> <span data-ttu-id="54491-117">Du kan holde styr på leveringskravene ved at oprette en leveranceplan.</span><span class="sxs-lookup"><span data-stu-id="54491-117">To keep track of the delivery requirements, you create a delivery schedule.</span></span> <span data-ttu-id="54491-118">Du kan oprette seks forskellige leverancelinjer på siden med leveranceplanen.</span><span class="sxs-lookup"><span data-stu-id="54491-118">On the delivery schedule page, you create six separate delivery lines.</span></span> <span data-ttu-id="54491-119">Hver leverancelinje indeholder 100 stole og angiver leveringsdatoen for disse 100 stole.</span><span class="sxs-lookup"><span data-stu-id="54491-119">Each delivery line contains 100 chairs and indicates the delivery date for those 100 chairs.</span></span> <span data-ttu-id="54491-120">I dette tilfælde modregnes hver linje på den første i måneden i seks på hinanden efterfølgende måneder.</span><span class="sxs-lookup"><span data-stu-id="54491-120">In this case, each line is offset on the first of the month for six consecutive months.</span></span>  

<span data-ttu-id="54491-121">Når du opretter en leveranceplan, ændres typen af den oprindelige ordrelinje automatisk til **Ordrelinje med flere leveringer**.</span><span class="sxs-lookup"><span data-stu-id="54491-121">When you create a delivery schedule, the type of the original order line is automatically changed to **Order line with multiple deliveries**.</span></span> <span data-ttu-id="54491-122">En linje af denne type kaldes en kommerciel linje og er markeret ved et ikon.</span><span class="sxs-lookup"><span data-stu-id="54491-122">A line of this type is referred to as a commercial line and is marked by an icon.</span></span> <span data-ttu-id="54491-123">Leveringslinjen er markeret ved et andet ikon.</span><span class="sxs-lookup"><span data-stu-id="54491-123">The delivery line is marked by a different icon.</span></span> <span data-ttu-id="54491-124">Hvis du ændrer et antal på en leverancelinje, opdateres den kommercielle linje til det samlede antal i leveranceplanen.</span><span class="sxs-lookup"><span data-stu-id="54491-124">If you change a quantity on a delivery line, the commercial line is updated to the total quantity of the delivery schedule.</span></span> <span data-ttu-id="54491-125">Hvis der i en samhandelsaftale er defineret en slutrabat for ordren, sørger leveranceplanen for, at din ordre bliver berettiget til slutrabatten, selv når ordren opdeles i adskilte leverancer.</span><span class="sxs-lookup"><span data-stu-id="54491-125">If a trade agreement has defined a total discount for the order, the delivery schedule ensures that your order is eligible for the total order discount, even when the order is split into separate deliveries.</span></span>  

<span data-ttu-id="54491-126">Ordrer, der har en leveranceplan, behandles i forhold til leverancelinjerne.</span><span class="sxs-lookup"><span data-stu-id="54491-126">Orders that have a delivery schedule are processed against the delivery lines.</span></span> <span data-ttu-id="54491-127">Behandling omfatter bogføringen af følgesedler, produktkvitteringer og fakturering.</span><span class="sxs-lookup"><span data-stu-id="54491-127">Processing includes the posting of packing slips, product receipts, and invoicing.</span></span>  

<span data-ttu-id="54491-128">Dokumentudskrifter af ordrer og tilbud, der har en leveranceplan, viser kun leverancelinjerne.</span><span class="sxs-lookup"><span data-stu-id="54491-128">Document printouts of orders and quotations that have a delivery schedule show only the delivery lines.</span></span> <span data-ttu-id="54491-129">De viser ikke de oprindelige linjer (kommercielle linjer).</span><span class="sxs-lookup"><span data-stu-id="54491-129">They don't show the original lines (commercial lines).</span></span> <span data-ttu-id="54491-130">**Bemærk:** Desuden er det kun leverancelinjerne, der vises i, når du udfører disse handlinger:</span><span class="sxs-lookup"><span data-stu-id="54491-130">**Note:** In addition, only the delivery lines are shown when you perform these actions:</span></span>

-   <span data-ttu-id="54491-131">Bogfør</span><span class="sxs-lookup"><span data-stu-id="54491-131">Post</span></span>
-   <span data-ttu-id="54491-132">Kopierer sider</span><span class="sxs-lookup"><span data-stu-id="54491-132">Copy pages</span></span>
-   <span data-ttu-id="54491-133">Gennemser listesider og rapporter</span><span class="sxs-lookup"><span data-stu-id="54491-133">Browse list pages and reports</span></span>

<span data-ttu-id="54491-134">Når du bekræfter salgstilbud, viser de oprettede salgsordrer hele leveranceplanen, også selvom ordrelinjerne har flere leverancer.</span><span class="sxs-lookup"><span data-stu-id="54491-134">When you confirm sales quotations, the resulting sales orders show the whole delivery schedule, even the order lines that have multiple deliveries.</span></span> <span data-ttu-id="54491-135">Hele leveranceplanen vises derudover på alle større sider, som f.eks. salgsordrer, salgstilbud og indkøbsordrer.</span><span class="sxs-lookup"><span data-stu-id="54491-135">In addition, the whole delivery schedule is shown on all the major pages, such as sales orders, sales quotations, and purchase orders.</span></span>




