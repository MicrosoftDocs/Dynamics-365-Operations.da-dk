---
title: Planlægge en produktionsordre
description: Denne procedure viser, hvordan du planlægger en produktionsordre.
author: johanhoffmann
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdSchedule, ProdRouteJob, WrkCtrCapResSum, ProdRouteJobSched, ProductionOrderScheduleDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8b3fe8f6890c7d8ac8835503091642faa773f7f6
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424588"
---
# <a name="schedule-a-production-order"></a><span data-ttu-id="17c2a-103">Planlægge en produktionsordre</span><span class="sxs-lookup"><span data-stu-id="17c2a-103">Schedule a production order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="17c2a-104">Denne procedure viser, hvordan du planlægger en produktionsordre.</span><span class="sxs-lookup"><span data-stu-id="17c2a-104">This procedure shows how to schedule a production order.</span></span> <span data-ttu-id="17c2a-105">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="17c2a-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="17c2a-106">Dette er den tredje procedure ud af syv, der beskriver produktionsordrelivscyklussen.</span><span class="sxs-lookup"><span data-stu-id="17c2a-106">This is the third procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="schedule-a-production-order"></a><span data-ttu-id="17c2a-107">Planlægge en produktionsordre</span><span class="sxs-lookup"><span data-stu-id="17c2a-107">Schedule a production order</span></span>
1. <span data-ttu-id="17c2a-108">Gå til Produktionsstyring > Produktionsordrer > Alle produktionsordrer.</span><span class="sxs-lookup"><span data-stu-id="17c2a-108">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="17c2a-109">Vælg en produktionsordre, som har statussen Forkalkuleret.</span><span class="sxs-lookup"><span data-stu-id="17c2a-109">Select a production order that has the Estimated status.</span></span>  
2. <span data-ttu-id="17c2a-110">Klik på Planlæg i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="17c2a-110">On the Action Pane, click Schedule.</span></span>
3. <span data-ttu-id="17c2a-111">Klik på Finplanlægge.</span><span class="sxs-lookup"><span data-stu-id="17c2a-111">Click Schedule jobs.</span></span>
    * <span data-ttu-id="17c2a-112">Parametrene for planlægning konfigureres på denne side.</span><span class="sxs-lookup"><span data-stu-id="17c2a-112">The parameters for scheduling are set up on this page.</span></span> <span data-ttu-id="17c2a-113">Du kan konfigurere parametre for bestemte brugere eller alle brugere.</span><span class="sxs-lookup"><span data-stu-id="17c2a-113">You can set up the parameters for specific users or all users.</span></span>  
4. <span data-ttu-id="17c2a-114">Vælg "Fremad fra i dag" i feltet Planlægningsvej.</span><span class="sxs-lookup"><span data-stu-id="17c2a-114">In the Scheduling direction field, select 'Forward from today'.</span></span>
5. <span data-ttu-id="17c2a-115">Angiv en dato i feltet Planlægningsdato.</span><span class="sxs-lookup"><span data-stu-id="17c2a-115">In the Scheduling date field, enter a date.</span></span>
6. <span data-ttu-id="17c2a-116">Markér eller fjern markeringen i afkrydsningsfeltet Kapacitetsbegrænsning.</span><span class="sxs-lookup"><span data-stu-id="17c2a-116">Select or clear the Finite capacity check box.</span></span>
7. <span data-ttu-id="17c2a-117">Markér eller fjern markeringen i afkrydsningsfeltet Materialebegrænsning.</span><span class="sxs-lookup"><span data-stu-id="17c2a-117">Select or clear the Finite material check box.</span></span>
8. <span data-ttu-id="17c2a-118">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="17c2a-118">Click OK.</span></span>

## <a name="view-the-scheduling-results"></a><span data-ttu-id="17c2a-119">Vise planlægningsresultaterne</span><span class="sxs-lookup"><span data-stu-id="17c2a-119">View the scheduling results</span></span>
1. <span data-ttu-id="17c2a-120">Klik på Produktionsordre i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="17c2a-120">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="17c2a-121">Klik på Alle job.</span><span class="sxs-lookup"><span data-stu-id="17c2a-121">Click All jobs.</span></span>
    * <span data-ttu-id="17c2a-122">Denne side viser de planlagte opgaver, som du lige har oprettet.</span><span class="sxs-lookup"><span data-stu-id="17c2a-122">This page displays the scheduled jobs that you have just generated.</span></span>  
3. <span data-ttu-id="17c2a-123">Udvid eller skjul sektionen Planlægning.</span><span class="sxs-lookup"><span data-stu-id="17c2a-123">Expand or collapse the Scheduling section.</span></span>
    * <span data-ttu-id="17c2a-124">Du kan få vist den planlagte dato og klokkeslæt i oversigtspanelet Planlægning.</span><span class="sxs-lookup"><span data-stu-id="17c2a-124">On the Scheduling FastTab, you can view the scheduled date and time.</span></span>  
4. <span data-ttu-id="17c2a-125">Klik på Forespørgsler.</span><span class="sxs-lookup"><span data-stu-id="17c2a-125">Click Inquiries.</span></span>
5. <span data-ttu-id="17c2a-126">Klik på Kapacitetsbelastning.</span><span class="sxs-lookup"><span data-stu-id="17c2a-126">Click Capacity load.</span></span>
    * <span data-ttu-id="17c2a-127">Siden Kapacitetsbelastning viser den kapacitet, der er reserveret via finplanlægning, det samlede antal timer, som aktuelt er reserveret for ressourcen, og antallet af timer, der er tilgængelige til finplanlægning af ressourcen.</span><span class="sxs-lookup"><span data-stu-id="17c2a-127">The Capacity load page displays the capacity that is reserved through job scheduling, the total number of hours that are currently reserved on the resource, and the number of hours that remain available for job scheduling on the resource.</span></span>  
6. <span data-ttu-id="17c2a-128">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="17c2a-128">Close the page.</span></span>
7. <span data-ttu-id="17c2a-129">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="17c2a-129">Close the page.</span></span>

