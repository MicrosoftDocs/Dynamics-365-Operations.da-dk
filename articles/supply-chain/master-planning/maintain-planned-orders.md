---
title: Vedligehold ordreforslag
description: Dette emne indeholder oplysninger om, hvordan du administrerer planlagte ordrer. Den beskriver, hvordan du kan opdatere status for planlagte ordrer, autorisere dem og filtrere for planlagte ordre, der har samme status som en valgte planlagt ordre.
author: roxanadiaconu
manager: AnnBe
ms.date: 11/07/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19151
ms.assetid: 54123f4c-b4ca-4ce4-9358-b067aa04c968
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 68bccb632255eac975dc150cf322d4c579ff2f24
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/18/2019
ms.locfileid: "2813770"
---
# <a name="maintain-planned-orders"></a><span data-ttu-id="cfb9f-104">Vedligehold ordreforslag</span><span class="sxs-lookup"><span data-stu-id="cfb9f-104">Maintain planned orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cfb9f-105">Dette emne indeholder oplysninger om, hvordan du administrerer planlagte ordrer.</span><span class="sxs-lookup"><span data-stu-id="cfb9f-105">This topic provides information about how to manage planned orders.</span></span> <span data-ttu-id="cfb9f-106">Den beskriver, hvordan du kan opdatere status for planlagte ordrer, autorisere dem og filtrere for planlagte ordre, der har samme status som en valgte planlagt ordre.</span><span class="sxs-lookup"><span data-stu-id="cfb9f-106">It describes how you can update the status of planned orders, firm them, and filter for planned orders that have the same status as a selected planned order.</span></span>

<span data-ttu-id="cfb9f-107">Du kan administrere ordreforslag fra arbejdsområdet **Varedisponering**, listen **Ordreforslag** eller listerne **Produktionsordreforslag**, **Planlagte indkøbsordrer** og **Planlagt overførsel**.</span><span class="sxs-lookup"><span data-stu-id="cfb9f-107">You can manage planned orders from the **Master planning** workspace, the **Planned order** list, or the **Planned production orders**, **Planned purchase orders**, and **Planned transfer** lists.</span></span> 

## <a name="planned-order-status"></a><span data-ttu-id="cfb9f-108">Status for ordreforslag</span><span class="sxs-lookup"><span data-stu-id="cfb9f-108">Planned order status</span></span>
<span data-ttu-id="cfb9f-109">Du kan bruge feltet **Status** til at registrere status.</span><span class="sxs-lookup"><span data-stu-id="cfb9f-109">You can use the **Status** field to help track your progress.</span></span> <span data-ttu-id="cfb9f-110">Følgende værdier bruges:</span><span class="sxs-lookup"><span data-stu-id="cfb9f-110">The following values are used:</span></span>

-   <span data-ttu-id="cfb9f-111">Når varedisponering opretter ordreforslag, har ordreforslagene statussen **Ubehandlet**.</span><span class="sxs-lookup"><span data-stu-id="cfb9f-111">When master planning generates planned orders, the planned orders have a status of **Unprocessed**.</span></span>
-   <span data-ttu-id="cfb9f-112">Hvis du vælger ikke at autorisere et ordreforslag, kan du tildele det statussen **Fuldført**.</span><span class="sxs-lookup"><span data-stu-id="cfb9f-112">If you decide not to firm a planned order, you can give it a status of **Completed**.</span></span>
-   <span data-ttu-id="cfb9f-113">Hvis du vil autorisere et ordreforslag, kan du ændre status til **Godkendt**.</span><span class="sxs-lookup"><span data-stu-id="cfb9f-113">If you want to firm a planned order, you can change the status to **Approved**.</span></span> <span data-ttu-id="cfb9f-114">Ordreforslag med statussen **Godkendt** respekteres af varedisponeringen, så de ikke ændres eller slettes, når varedisponeringen køres.</span><span class="sxs-lookup"><span data-stu-id="cfb9f-114">Planned orders with **Approved** status are respected by master planning, so they are not modified or deleted during a later master planning run.</span></span> 

## <a name="firming-planned-orders"></a><span data-ttu-id="cfb9f-115">Autorisering af ordreforslag</span><span class="sxs-lookup"><span data-stu-id="cfb9f-115">Firming planned orders</span></span> 
<span data-ttu-id="cfb9f-116">Når ordreforslag autoriseres, oprettes rigtige ordrer.</span><span class="sxs-lookup"><span data-stu-id="cfb9f-116">By firming planned orders, real orders are created.</span></span> <span data-ttu-id="cfb9f-117">Disse kaldes også *frigivne* eller *åbne ordrer*.</span><span class="sxs-lookup"><span data-stu-id="cfb9f-117">These are also know as *released* or *open orders*.</span></span> <span data-ttu-id="cfb9f-118">Når et ordreforslag er autoriseret, flyttes det til ordresektionen i det relevante modul.</span><span class="sxs-lookup"><span data-stu-id="cfb9f-118">When a planned order is firmed, it's moved to the orders section of the relevant module.</span></span>

<span data-ttu-id="cfb9f-119">Du kan vælge to autorisationsindstillinger på siden **Ordreforslag**:</span><span class="sxs-lookup"><span data-stu-id="cfb9f-119">You can select two firming options from the **Planned orders** page:</span></span>

-   <span data-ttu-id="cfb9f-120">**Autoriser** – Dette autoriserer et eller flere valgte ordreforslag.</span><span class="sxs-lookup"><span data-stu-id="cfb9f-120">**Firm** – This will firm one or multiple selected planned orders.</span></span>
-   <span data-ttu-id="cfb9f-121">**Autoriser alle** – Dette autoriserer alle ordreforslag i filteret.</span><span class="sxs-lookup"><span data-stu-id="cfb9f-121">**Firm all** – This will firm all planned orders in the filter.</span></span> <span data-ttu-id="cfb9f-122">Når du bruger **Autoriser alle**, behøver du ikke vælge ordreforslaget, da alle ordreforslag i filtret autoriseres.</span><span class="sxs-lookup"><span data-stu-id="cfb9f-122">Using **Firm all** you don’t have to select the planned order, all planned orders within the filter will be firmed.</span></span> <span data-ttu-id="cfb9f-123">Denne indstilling kan være nyttig, hvis du skal autorisere et stort antal ordreforslag.</span><span class="sxs-lookup"><span data-stu-id="cfb9f-123">This option can be useful if you are firming a high number of planned orders.</span></span>

> [!NOTE]
> <span data-ttu-id="cfb9f-124">Du kan spore et ordreforslag, der er autoriseret, fra **Autorisationshistorik** under **formen Ordreforslag > Vis > Autorisationshistorik**.</span><span class="sxs-lookup"><span data-stu-id="cfb9f-124">You can track a planned order that was firmed from **Firming history** under **Planned orders form > View > Firming history**.</span></span>

## <a name="parallelize-firming"></a><span data-ttu-id="cfb9f-125">Parallel autorisation</span><span class="sxs-lookup"><span data-stu-id="cfb9f-125">Parallelize firming</span></span>
<span data-ttu-id="cfb9f-126">Hvis du planlægger at autorisere mange ordrer på samme tid, kan parallelisering af afviklingen forbedre kørselstiden eller ydeevnen.</span><span class="sxs-lookup"><span data-stu-id="cfb9f-126">If you are planning to firm many orders at the same time, parallelizing the run can improve the run time or performance.</span></span> <span data-ttu-id="cfb9f-127">Denne indstilling er tilgængelig, når der autoriseres flere ordreforslag med enten **Autoriser** eller **Autoriser alle**.</span><span class="sxs-lookup"><span data-stu-id="cfb9f-127">This option is available when firming multiple planned orders with either **Firm** or **Firm all**.</span></span> <span data-ttu-id="cfb9f-128">Følgende parametre er tilgængelige:</span><span class="sxs-lookup"><span data-stu-id="cfb9f-128">The following parameters are available:</span></span>

-   <span data-ttu-id="cfb9f-129">**Paralleliser autorisation** – Hvis den er **Ja**, vil autorisationsprocessen blive parallel med det antal tråde, der er defineret i **Antal tråde**.</span><span class="sxs-lookup"><span data-stu-id="cfb9f-129">**Parallelize firming** – If **Yes**, the firming process will be parallelized with the number of threads defined in **Number of threads**.</span></span>
-   <span data-ttu-id="cfb9f-130">**Antal tråde** – Styrer antallet af tråde, der bruges til at parallelisere autorisationsprocessen.</span><span class="sxs-lookup"><span data-stu-id="cfb9f-130">**Number of threads** – Controls the number of threads used to parallelize the firming process.</span></span> <span data-ttu-id="cfb9f-131">Parameteren vises kun, når **Paralleliser autorisation** er angivet til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="cfb9f-131">The parameter is only shown when **Parallelize firming** is set to **Yes**.</span></span>


<a name="additional-resources"></a><span data-ttu-id="cfb9f-132">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="cfb9f-132">Additional resources</span></span>
--------

[<span data-ttu-id="cfb9f-133">Oversigt over behovsplaner</span><span class="sxs-lookup"><span data-stu-id="cfb9f-133">Master plans overview</span></span>](master-plans.md)



