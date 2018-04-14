--- 
title: "Rapportere som færdig til en id-styret lokalitet"
description: "Denne opgavevejledning viser et eksempel på færdigmedling til en lokation, der ikke er id-kontrolleret."
author: ChristianRytt
manager: AnnBe
ms.date: 06/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 9a7901b307cffb81cce351e4e45ac8f73f328b02
ms.contentlocale: da-dk
ms.lasthandoff: 04/13/2018

---
# <a name="report-as-finished-to-a-plate-controlled-location"></a><span data-ttu-id="831d7-103">Rapportere som færdig til en id-styret lokalitet</span><span class="sxs-lookup"><span data-stu-id="831d7-103">Report as finished to a plate-controlled location</span></span> 

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="831d7-104">Denne opgavevejledning viser et eksempel på færdigmedling til en lokation, der ikke er id-kontrolleret.</span><span class="sxs-lookup"><span data-stu-id="831d7-104">This task guide shows an example of reporting as finished to a location that isn't license plate–controlled.</span></span> <span data-ttu-id="831d7-105">En relevant arbejdspolitik er en forudsætning for denne opgave.</span><span class="sxs-lookup"><span data-stu-id="831d7-105">An applicable work policy is the prerequisite for this task.</span></span> <span data-ttu-id="831d7-106">En tidligere opgavevejledning viste konfigurationen af arbejdspolitikken.</span><span class="sxs-lookup"><span data-stu-id="831d7-106">A previous task guide showed the setup of the work policy.</span></span> <span data-ttu-id="831d7-107">Denne opgavevejledning kræver Dynamics AX-program 7.0.1 eller nyere.</span><span class="sxs-lookup"><span data-stu-id="831d7-107">This task guide requires Dynamics AX application 7.0.1 or later.</span></span>




## <a name="set-up-an-output-location"></a><span data-ttu-id="831d7-108">Konfigurere en outputlokation</span><span class="sxs-lookup"><span data-stu-id="831d7-108">Set up an output location</span></span>
1. <span data-ttu-id="831d7-109">Gå til Virksomhedsadministration > Ressourcer > Ressourcegrupper.</span><span class="sxs-lookup"><span data-stu-id="831d7-109">Go to Organization administration > Resources > Resource groups.</span></span>
2. <span data-ttu-id="831d7-110">Vælg ressourcegruppen '5102' på listen.</span><span class="sxs-lookup"><span data-stu-id="831d7-110">In the list, select resource group '5102'.</span></span>
3. <span data-ttu-id="831d7-111">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="831d7-111">Click Edit.</span></span>
4. <span data-ttu-id="831d7-112">Indtast '51' i feltet Lagersted for udlagring.</span><span class="sxs-lookup"><span data-stu-id="831d7-112">In the Output warehouse field, enter '51'.</span></span>
5. <span data-ttu-id="831d7-113">Indtast '001' i feltet Udlagringslokation.</span><span class="sxs-lookup"><span data-stu-id="831d7-113">In the Output location field, enter '001'.</span></span>
    * <span data-ttu-id="831d7-114">Lokationen 001 er ikke en id-kontrolleret lokation.</span><span class="sxs-lookup"><span data-stu-id="831d7-114">Location 001 isn't a license plate–controlled location.</span></span> <span data-ttu-id="831d7-115">Du kan kun konfigurere en outputplacering uden id-kontrol, hvis der findes en gyldig arbejdspolitik for lokationen.</span><span class="sxs-lookup"><span data-stu-id="831d7-115">You can set up a non–license plate output location only if an applicable work policy exists for the location.</span></span>  

## <a name="create-a-production-order-and-report-it-as-finished"></a><span data-ttu-id="831d7-116">Oprette en produktionsordre og rapportere den som færdig</span><span class="sxs-lookup"><span data-stu-id="831d7-116">Create a production order and report it as finished</span></span>
1. <span data-ttu-id="831d7-117">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="831d7-117">Close the page.</span></span>
2. <span data-ttu-id="831d7-118">Gå til Produktionsstyring > Produktionsordrer > Alle produktionsordrer.</span><span class="sxs-lookup"><span data-stu-id="831d7-118">Go to Production control > Production orders > All production orders.</span></span>
3. <span data-ttu-id="831d7-119">Klik på Ny produktionsordre.</span><span class="sxs-lookup"><span data-stu-id="831d7-119">Click New production order.</span></span>
4. <span data-ttu-id="831d7-120">Indtast 'L0101' i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="831d7-120">In the Item number field, enter 'L0101'.</span></span>
5. <span data-ttu-id="831d7-121">Klik på Opret.</span><span class="sxs-lookup"><span data-stu-id="831d7-121">Click Create.</span></span>
6. <span data-ttu-id="831d7-122">Klik på Produktionsordre i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="831d7-122">On the Action Pane, click Production order.</span></span>
7. <span data-ttu-id="831d7-123">Klik på Forkalkulation.</span><span class="sxs-lookup"><span data-stu-id="831d7-123">Click Estimate.</span></span>
8. <span data-ttu-id="831d7-124">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="831d7-124">Click OK.</span></span>
9. <span data-ttu-id="831d7-125">Klik på Start.</span><span class="sxs-lookup"><span data-stu-id="831d7-125">Click Start.</span></span>
10. <span data-ttu-id="831d7-126">Klik på fanen Generelt.</span><span class="sxs-lookup"><span data-stu-id="831d7-126">Click the General tab.</span></span>
11. <span data-ttu-id="831d7-127">Vælg "Aldrig" i feltet Automatisk styklisteforbrug.</span><span class="sxs-lookup"><span data-stu-id="831d7-127">In the Automatic BOM consumption field, select 'Never'.</span></span>
12. <span data-ttu-id="831d7-128">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="831d7-128">Click OK.</span></span>
13. <span data-ttu-id="831d7-129">Klik på Færdigmeld.</span><span class="sxs-lookup"><span data-stu-id="831d7-129">Click Report as finished.</span></span>
14. <span data-ttu-id="831d7-130">Klik på fanen Generelt.</span><span class="sxs-lookup"><span data-stu-id="831d7-130">Click the General tab.</span></span>
15. <span data-ttu-id="831d7-131">Vælg Ja i feltet Accepter fejl.</span><span class="sxs-lookup"><span data-stu-id="831d7-131">Select Yes in the Accept error field.</span></span>
16. <span data-ttu-id="831d7-132">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="831d7-132">Click OK.</span></span>
17. <span data-ttu-id="831d7-133">Klik på Lagersted i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="831d7-133">On the Action Pane, click Warehouse.</span></span>
18. <span data-ttu-id="831d7-134">Klik på Arbejdsdetaljer.</span><span class="sxs-lookup"><span data-stu-id="831d7-134">Click Work details.</span></span>
    * <span data-ttu-id="831d7-135">Når produktionsordren er færdigmeldt, oprettes der intet arbejde for læg-på-lager.</span><span class="sxs-lookup"><span data-stu-id="831d7-135">When the production order was reported as finished, no work was generated for put-away.</span></span> <span data-ttu-id="831d7-136">Dette skyldes, at der er defineret en arbejdspolitik, som forhindrer, at der genereres arbejde, når produktet L0101 rapporteres som færdigt på lokation 001.</span><span class="sxs-lookup"><span data-stu-id="831d7-136">This occurs because a work policy is defined that prevents work from being generated when product L0101 is reported as finished to location 001.</span></span>  


