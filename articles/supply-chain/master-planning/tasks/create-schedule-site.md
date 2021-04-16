---
title: Oprette en tidsplan for et sted
description: Denne procedure viser, hvordan du planlægger produktionsordrer, der endnu ikke er startet på en lokation.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTableListPage, ProdSchedule, ProdRouteJob
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 070d8441700cd0051d421ea7e2210bcb668e8c22
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820364"
---
# <a name="create-a-schedule-for-a-site"></a><span data-ttu-id="8b587-103">Oprette en tidsplan for et sted</span><span class="sxs-lookup"><span data-stu-id="8b587-103">Create a schedule for a site</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8b587-104">Denne procedure viser, hvordan du planlægger produktionsordrer, der endnu ikke er startet på en lokation.</span><span class="sxs-lookup"><span data-stu-id="8b587-104">This procedure shows how to schedule production orders that are not yet started for a site.</span></span>  <span data-ttu-id="8b587-105">Demodatafirmaet USMF bruges til at fuldføre denne procedure.</span><span class="sxs-lookup"><span data-stu-id="8b587-105">The demo data company USMF is used to complete this procedure.</span></span>


## <a name="identify-production-orders-that-are-not-started"></a><span data-ttu-id="8b587-106">Identificere produktionsordrer, der ikke er startet</span><span class="sxs-lookup"><span data-stu-id="8b587-106">Identify production orders that are not started</span></span>
1. <span data-ttu-id="8b587-107">Gå til Produktionsstyring > Produktionsordrer > Alle produktionsordrer.</span><span class="sxs-lookup"><span data-stu-id="8b587-107">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="8b587-108">Brug Quick Filter til at finde poster.</span><span class="sxs-lookup"><span data-stu-id="8b587-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="8b587-109">Du kan f.eks. filtrere på feltet Lokation med værdien '1'.</span><span class="sxs-lookup"><span data-stu-id="8b587-109">For example, filter on the Site field with a value of '1'.</span></span>
    * <span data-ttu-id="8b587-110">1 repræsenterer en lokation i USMF.</span><span class="sxs-lookup"><span data-stu-id="8b587-110">1 represents a site in USMF.</span></span> <span data-ttu-id="8b587-111">Hvis du ikke bruger USMF, kan du vælge en lokation fra din egen virksomhed.</span><span class="sxs-lookup"><span data-stu-id="8b587-111">If you are not using USMF, select a site from your own company.</span></span>  
3. <span data-ttu-id="8b587-112">Åbn kolonnefilteret Status.</span><span class="sxs-lookup"><span data-stu-id="8b587-112">Open the Status column filter.</span></span>
4. <span data-ttu-id="8b587-113">Anvend et filter for feltet "Status" med værdien "Planlagt" ved hjælp af filteroperatøren "er præcis".</span><span class="sxs-lookup"><span data-stu-id="8b587-113">Apply a filter on the "Status" field, with a value of "Scheduled", using the "is exactly" filter operator.</span></span>

## <a name="create-a-schedule"></a><span data-ttu-id="8b587-114">Oprette en tidsplan</span><span class="sxs-lookup"><span data-stu-id="8b587-114">Create a schedule</span></span>
1. <span data-ttu-id="8b587-115">Markér eller fjern markeringen af alle rækker på listen.</span><span class="sxs-lookup"><span data-stu-id="8b587-115">In the list, mark or unmark all rows.</span></span>
2. <span data-ttu-id="8b587-116">Klik på Planlæg i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="8b587-116">On the Action Pane, click Schedule.</span></span>
3. <span data-ttu-id="8b587-117">Klik på Finplanlægge.</span><span class="sxs-lookup"><span data-stu-id="8b587-117">Click Schedule jobs.</span></span>
4. <span data-ttu-id="8b587-118">Vælg 'Bagud fra leveringsdato' i feltet Planlægningsvej.</span><span class="sxs-lookup"><span data-stu-id="8b587-118">In the Scheduling direction field, select 'Backward from delivery date'.</span></span>
5. <span data-ttu-id="8b587-119">Vælg Nej i feltet Kapacitetsbegrænsning.</span><span class="sxs-lookup"><span data-stu-id="8b587-119">Select No in the Finite capacity field.</span></span>
6. <span data-ttu-id="8b587-120">Vælg Nej i feltet Materialebegrænsning.</span><span class="sxs-lookup"><span data-stu-id="8b587-120">Select No in the Finite material field.</span></span>
7. <span data-ttu-id="8b587-121">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="8b587-121">Click OK.</span></span>
    * <span data-ttu-id="8b587-122">Det kan tage et stykke tid.</span><span class="sxs-lookup"><span data-stu-id="8b587-122">This may take a while.</span></span>  

## <a name="view-the-result-of-scheduled-production-orders"></a><span data-ttu-id="8b587-123">Vise resultatet af planlagte produktionsordrer</span><span class="sxs-lookup"><span data-stu-id="8b587-123">View the result of scheduled production orders</span></span>
1. <span data-ttu-id="8b587-124">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="8b587-124">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="8b587-125">Du kan markere enhver række.</span><span class="sxs-lookup"><span data-stu-id="8b587-125">You can mark any row.</span></span>  
2. <span data-ttu-id="8b587-126">Klik på Produktionsordre i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="8b587-126">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="8b587-127">Klik på Alle job.</span><span class="sxs-lookup"><span data-stu-id="8b587-127">Click All jobs.</span></span>
    * <span data-ttu-id="8b587-128">På denne side kan du se listen over job.</span><span class="sxs-lookup"><span data-stu-id="8b587-128">On this page, you can see the list of jobs.</span></span> <span data-ttu-id="8b587-129">Under fanen planlægning kan du se startdatoen og slutdatoen for et job.</span><span class="sxs-lookup"><span data-stu-id="8b587-129">On the Scheduling tab, you can see the Start date and End date for a job.</span></span>  
4. <span data-ttu-id="8b587-130">Klik på Materialer.</span><span class="sxs-lookup"><span data-stu-id="8b587-130">Click Materials.</span></span>
    * <span data-ttu-id="8b587-131">På denne side kan du se det forkalkulerede materialeforbrug for operationer på produktionsordren og den aktuelle disponible beholdning.</span><span class="sxs-lookup"><span data-stu-id="8b587-131">On this page, you can see the estimated material consumption for the operations on the production order and the current available inventory.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]