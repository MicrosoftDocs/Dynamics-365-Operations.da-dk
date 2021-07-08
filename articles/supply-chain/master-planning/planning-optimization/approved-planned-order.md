---
title: Vise, administrere og godkende ordreforslag
description: Dette emne beskriver, hvordan du kan få vist, administrere og godkende ordreforslag i Planlægningsoptimering.
author: ChristianRytt
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-08-21
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 71ec26bea2063bcf8b6d302a7ece804b3ac934b3
ms.sourcegitcommit: 3673eeca1ada0f3e4ec277176515a946706f8a41
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/24/2021
ms.locfileid: "6304361"
---
# <a name="view-manage-and-approve-planned-orders"></a><span data-ttu-id="662fe-103">Vise, administrere og godkende ordreforslag</span><span class="sxs-lookup"><span data-stu-id="662fe-103">View, manage, and approve planned orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="662fe-104">Dette emne beskriver, hvordan du kan få vist, administrere og godkende ordreforslag i Planlægningsoptimering.</span><span class="sxs-lookup"><span data-stu-id="662fe-104">This topic provides information about how to view, manage, and approve planned orders in Planning Optimization.</span></span>

## <a name="view-and-manage-planned-orders"></a><a name="view-planned-orders"></a><span data-ttu-id="662fe-105">Vise og administrere ordreforslag</span><span class="sxs-lookup"><span data-stu-id="662fe-105">View and manage planned orders</span></span>

<span data-ttu-id="662fe-106">Du kan få vist og administrere ordreforslag på enhver listeside med ordreforslag.</span><span class="sxs-lookup"><span data-stu-id="662fe-106">You can view and manage planned orders on any planned orders list page.</span></span> <span data-ttu-id="662fe-107">Gå til et af følgende steder, afhængigt af hvilken type ordreforslag du vil arbejde med:</span><span class="sxs-lookup"><span data-stu-id="662fe-107">Go to one of the following places, depending on the type of planned orders that you want to work with:</span></span>

- <span data-ttu-id="662fe-108">Varedisponering \> Arbejdsområder \> Varedisponering</span><span class="sxs-lookup"><span data-stu-id="662fe-108">Master planning \> Workspaces \> Master planning</span></span>
- <span data-ttu-id="662fe-109">Varedisponering \> Varedisponering \> Ordreforslag</span><span class="sxs-lookup"><span data-stu-id="662fe-109">Master planning \> Master planning \> Planned orders</span></span>
- <span data-ttu-id="662fe-110">Produktionsstyring \> Produktionsordrer \> Produktionsordreforslag</span><span class="sxs-lookup"><span data-stu-id="662fe-110">Production control \> Production orders \> Planned production orders</span></span>
- <span data-ttu-id="662fe-111">Indkøb og forsyning \> Indkøbsordrer \> Indkøbsordreforslag</span><span class="sxs-lookup"><span data-stu-id="662fe-111">Procurement and sourcing \> Purchase orders \> Planned purchase orders</span></span>
- <span data-ttu-id="662fe-112">Lagerstyring \> Indgående ordrer \> Overførselsforslag</span><span class="sxs-lookup"><span data-stu-id="662fe-112">Inventory management \> Inbound orders \> Planned transfers</span></span>
- <span data-ttu-id="662fe-113">Lagerstyring \> Udgående ordrer \> Overførselsforslag</span><span class="sxs-lookup"><span data-stu-id="662fe-113">Inventory management \> Outbound orders \> Planned transfers</span></span>

## <a name="view-and-edit-the-status-of-planned-orders"></a><span data-ttu-id="662fe-114">Få vist og redigere status for ordreforslag</span><span class="sxs-lookup"><span data-stu-id="662fe-114">View and edit the status of planned orders</span></span>

<span data-ttu-id="662fe-115">Du kan bruge feltet **Status** i hvert ordreforslag til at spore forløbet eller ændre behandlingen af et ordreforslag.</span><span class="sxs-lookup"><span data-stu-id="662fe-115">You can use the **Status** field of each planned order to help track your progress or change how a planned order will be processed.</span></span> <span data-ttu-id="662fe-116">Følgende værdier for **Status** er tilgængelige:</span><span class="sxs-lookup"><span data-stu-id="662fe-116">The following **Status** values are available:</span></span>

- <span data-ttu-id="662fe-117">**Ubehandlet** – Når varedisponeringen opretter ordreforslag, tildeles de denne status.</span><span class="sxs-lookup"><span data-stu-id="662fe-117">**Unprocessed** – When master planning generates planned orders, they are given this status.</span></span> <span data-ttu-id="662fe-118">Ordreforslag med denne status vil blive slettet under næste planlægningskørsel.</span><span class="sxs-lookup"><span data-stu-id="662fe-118">Planned orders that have this status will be deleted during the next planning run.</span></span>
- <span data-ttu-id="662fe-119">**Fuldført** – Denne status angiver, at ordreforslaget er fuldført.</span><span class="sxs-lookup"><span data-stu-id="662fe-119">**Completed** – This status indicates that the planned order has been completed.</span></span> <span data-ttu-id="662fe-120">Hvis du vælger ikke at autorisere et ordreforslag, kan du ændre dets status manuelt til *Fuldført*.</span><span class="sxs-lookup"><span data-stu-id="662fe-120">If you decide not to firm a planned order, you can manually change its status to *Completed*.</span></span> <span data-ttu-id="662fe-121">Bemærk, at systemet behandler statussen som *Ubehandlet* og *Fuldført* på samme måde.</span><span class="sxs-lookup"><span data-stu-id="662fe-121">Note that the system treats the *Unprocessed* and *Completed* statuses in the same way.</span></span>
- <span data-ttu-id="662fe-122">**Godkendt** – Denne status angiver, at ordreforslaget er godkendt til autorisation.</span><span class="sxs-lookup"><span data-stu-id="662fe-122">**Approved** – This status indicates that the planned order is approved for firming.</span></span> <span data-ttu-id="662fe-123">Hvis du vil autorisere et ordreforslag, kan du ændre dets status til *Godkendt*.</span><span class="sxs-lookup"><span data-stu-id="662fe-123">If you want to firm a planned order, you can change its status to *Approved*.</span></span> <span data-ttu-id="662fe-124">Hvis du vil bevare ændringerne af et ordreforslag, eller hvis du planlægger at autoriseret et ordreforslag, skal du ændre dets status til *Godkendt*.</span><span class="sxs-lookup"><span data-stu-id="662fe-124">If you want to keep the edits that have been made to a planned order, or if you're planning to firm a planned order, change its status to *Approved*.</span></span> <span data-ttu-id="662fe-125">Ordreforslag med statussen *Godkendt* betragtes som fast og forventet forsyning gennem varedisponering.</span><span class="sxs-lookup"><span data-stu-id="662fe-125">Planned orders that have a status of *Approved* are considered fixed and expected supply by master planning.</span></span> <span data-ttu-id="662fe-126">Derfor ændres eller slettes de ikke under senere kørsler af varedisponeringen.</span><span class="sxs-lookup"><span data-stu-id="662fe-126">Therefore, they aren't modified or deleted during later master planning runs.</span></span> <span data-ttu-id="662fe-127">For at opnå dette kopierer planlægningslogikken ordreforslag med statussen *Godkendt* fra den gamle planversion til den nye planversion under varedisponeringen.</span><span class="sxs-lookup"><span data-stu-id="662fe-127">To achieve this behavior, the planning logic copies planned orders that have a status of *Approved* from the old plan version to the new plan version during master planning.</span></span> <span data-ttu-id="662fe-128">Bemærk, at ordreforslag med statussen *Godkendt* kun betragtes som forsyning inden for den specifikke behovsplan.</span><span class="sxs-lookup"><span data-stu-id="662fe-128">Note that planned orders that have a status of *Approved* are considered supply only within the specific master plan.</span></span>

<span data-ttu-id="662fe-129">Hvis du vil ændre statussen for et enkelt ordreforslag, skal du [åbne en listeside med ordreforslag](#view-planned-orders), åbne ordren og derefter benytte en af følgende fremgangsmåder:</span><span class="sxs-lookup"><span data-stu-id="662fe-129">To change the status of a single planned order, [open any planned orders list page](#view-planned-orders), open the order, and then follow one of these steps:</span></span>

- <span data-ttu-id="662fe-130">Rediger værdien i feltet **Status** i oversigtspanelet **Generelt**.</span><span class="sxs-lookup"><span data-stu-id="662fe-130">On the **General** FastTab, change the value of the **Status** field.</span></span>
- <span data-ttu-id="662fe-131">Vælg **Skift status** i gruppen **Proces** under fanen **Ordreforslag** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="662fe-131">On the Action Pane, on the **Planned order** tab, in the **Process** group, select **Change status**.</span></span>
- <span data-ttu-id="662fe-132">Hvis du vil markere ordren som godkendt, skal du vælge **Godkend** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="662fe-132">On the Action Pane, select **Approve** to mark the order as approved.</span></span>

<span data-ttu-id="662fe-133">Hvis du vil ændre statussen for flere ordreforslag på én gang, skal du [åbne en listeside med ordreforslag](#view-planned-orders), markere afkrydsningsfeltet for hver ordre, som du vil ændre, og derefter benytte en af følgende fremgangsmåder:</span><span class="sxs-lookup"><span data-stu-id="662fe-133">To change the status of several planned orders at the same time, [open any planned orders list page](#view-planned-orders), select the check box for each order that you want to change, and then follow one of these steps:</span></span>

- <span data-ttu-id="662fe-134">Vælg **Skift status** i gruppen **Proces** under fanen **Ordreforslag** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="662fe-134">On the Action Pane, on the **Planned order** tab, in the **Process** group, select **Change status**.</span></span>
- <span data-ttu-id="662fe-135">Hvis du vil markere ordrerne som godkendt, skal du vælge **Godkend** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="662fe-135">On the Action Pane, select **Approve** to mark the orders as approved.</span></span>

## <a name="approve-planned-orders"></a><span data-ttu-id="662fe-136">Godkende ordreforslag</span><span class="sxs-lookup"><span data-stu-id="662fe-136">Approve planned orders</span></span>

<span data-ttu-id="662fe-137">Godkendelse af ordreforslag er et valgfrit trin i processen for oprettelse af en autoriseret ordre fra et ordreforslag.</span><span class="sxs-lookup"><span data-stu-id="662fe-137">Approval of planned orders is an optional step in the process of creating a firmed order from a planned order.</span></span>

<span data-ttu-id="662fe-138">Følgende illustration viser, hvordan du kan bruge den værdi for **Status**, som er tildelt det enkelte ordreforslag, til at implementere en arbejdsproces for godkendelse.</span><span class="sxs-lookup"><span data-stu-id="662fe-138">The following illustration shows how you can use the **Status** value that is assigned to each planned order to implement an approval workflow.</span></span> <span data-ttu-id="662fe-139">Hvis du vil implementere en godkendelsesproces, skal dujustere værdien for **Status** manuelt for det enkelte ordreforslag som beskrevet i forrige afsnit.</span><span class="sxs-lookup"><span data-stu-id="662fe-139">To implement an approval process, manually adjust the **Status** value for each planned order as described in the previous section.</span></span>

![Ordreforslagsflow](media/approved-planned-orders-1.png)

> [!TIP]
> <span data-ttu-id="662fe-141">Det anbefales, at du godkender eventuelle ændrede ordreforslag.</span><span class="sxs-lookup"><span data-stu-id="662fe-141">We recommend that you approve any modified planned orders.</span></span> <span data-ttu-id="662fe-142">Ellers ignoreres og overskrives ændringerne i næste planlægningskørsel.</span><span class="sxs-lookup"><span data-stu-id="662fe-142">Otherwise, the edits will be ignored and overwritten by the next planning run.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="662fe-143">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="662fe-143">Additional resources</span></span>

- [<span data-ttu-id="662fe-144">Autoriser ordreforslag</span><span class="sxs-lookup"><span data-stu-id="662fe-144">Firm planned orders</span></span>](planned-order-firming.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
