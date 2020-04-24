---
title: Færdigmelde til en ikke-id-styret lokation (program, maj 2016)
description: Denne opgavevejledning viser et eksempel på færdigmedling til en lokation, der ikke er id-kontrolleret.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrResourceGroup, ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdParmCostEstimation, ProdParmStartUp, ProdParmReportFinished, WHSWorkTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5a9010b95cfd0528cd3b532627d19a3b340bdca4
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3210565"
---
# <a name="report-as-finished-to-a-non-license-plate-controlled-location--application-may-2016"></a><span data-ttu-id="dad2e-103">Færdigmelde til en ikke-id-styret lokation (program, maj 2016)</span><span class="sxs-lookup"><span data-stu-id="dad2e-103">Report as finished to a non-license plate controlled location  (Application, May 2016)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dad2e-104">Denne opgavevejledning viser et eksempel på færdigmedling til en lokation, der ikke er id-kontrolleret.</span><span class="sxs-lookup"><span data-stu-id="dad2e-104">This task guide shows an example of reporting as finished to a location that isn't license plate–controlled.</span></span> <span data-ttu-id="dad2e-105">En relevant arbejdspolitik er en forudsætning for denne opgave.</span><span class="sxs-lookup"><span data-stu-id="dad2e-105">An applicable work policy is the prerequisite for this task.</span></span> <span data-ttu-id="dad2e-106">En tidligere opgavevejledning viste konfigurationen af arbejdspolitikken.</span><span class="sxs-lookup"><span data-stu-id="dad2e-106">A previous task guide showed the setup of the work policy.</span></span> <span data-ttu-id="dad2e-107">Denne opgavevejledning kræver Dynamics AX-program 7.0.1 eller nyere.</span><span class="sxs-lookup"><span data-stu-id="dad2e-107">This task guide requires Dynamics AX application 7.0.1 or later.</span></span>




## <a name="set-up-an-output-location"></a><span data-ttu-id="dad2e-108">Konfigurere en outputlokation</span><span class="sxs-lookup"><span data-stu-id="dad2e-108">Set up an output location</span></span>
1. <span data-ttu-id="dad2e-109">Gå til Virksomhedsadministration > Ressourcer > Ressourcegrupper.</span><span class="sxs-lookup"><span data-stu-id="dad2e-109">Go to Organization administration > Resources > Resource groups.</span></span>
2. <span data-ttu-id="dad2e-110">Vælg ressourcegruppen '5102' på listen.</span><span class="sxs-lookup"><span data-stu-id="dad2e-110">In the list, select resource group '5102'.</span></span>
3. <span data-ttu-id="dad2e-111">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="dad2e-111">Click Edit.</span></span>
4. <span data-ttu-id="dad2e-112">Indtast '51' i feltet Lagersted for udlagring.</span><span class="sxs-lookup"><span data-stu-id="dad2e-112">In the Output warehouse field, enter '51'.</span></span>
5. <span data-ttu-id="dad2e-113">Indtast '001' i feltet Udlagringslokation.</span><span class="sxs-lookup"><span data-stu-id="dad2e-113">In the Output location field, enter '001'.</span></span>
    * <span data-ttu-id="dad2e-114">Lokationen 001 er ikke en id-kontrolleret lokation.</span><span class="sxs-lookup"><span data-stu-id="dad2e-114">Location 001 isn't a license plate–controlled location.</span></span> <span data-ttu-id="dad2e-115">Du kan kun konfigurere en outputplacering uden id-kontrol, hvis der findes en gyldig arbejdspolitik for lokationen.</span><span class="sxs-lookup"><span data-stu-id="dad2e-115">You can set up a non–license plate output location only if an applicable work policy exists for the location.</span></span>  

## <a name="create-a-production-order-and-report-it-as-finished"></a><span data-ttu-id="dad2e-116">Oprette en produktionsordre og rapportere den som færdig</span><span class="sxs-lookup"><span data-stu-id="dad2e-116">Create a production order and report it as finished</span></span>
1. <span data-ttu-id="dad2e-117">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="dad2e-117">Close the page.</span></span>
2. <span data-ttu-id="dad2e-118">Gå til Produktionsstyring > Produktionsordrer > Alle produktionsordrer.</span><span class="sxs-lookup"><span data-stu-id="dad2e-118">Go to Production control > Production orders > All production orders.</span></span>
3. <span data-ttu-id="dad2e-119">Klik på Ny produktionsordre.</span><span class="sxs-lookup"><span data-stu-id="dad2e-119">Click New production order.</span></span>
4. <span data-ttu-id="dad2e-120">Indtast 'L0101' i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="dad2e-120">In the Item number field, enter 'L0101'.</span></span>
5. <span data-ttu-id="dad2e-121">Klik på Opret.</span><span class="sxs-lookup"><span data-stu-id="dad2e-121">Click Create.</span></span>
6. <span data-ttu-id="dad2e-122">Klik på Produktionsordre i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="dad2e-122">On the Action Pane, click Production order.</span></span>
7. <span data-ttu-id="dad2e-123">Klik på Forkalkulation.</span><span class="sxs-lookup"><span data-stu-id="dad2e-123">Click Estimate.</span></span>
8. <span data-ttu-id="dad2e-124">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="dad2e-124">Click OK.</span></span>
9. <span data-ttu-id="dad2e-125">Klik på Start.</span><span class="sxs-lookup"><span data-stu-id="dad2e-125">Click Start.</span></span>
10. <span data-ttu-id="dad2e-126">Klik på fanen Generelt.</span><span class="sxs-lookup"><span data-stu-id="dad2e-126">Click the General tab.</span></span>
11. <span data-ttu-id="dad2e-127">Vælg "Aldrig" i feltet Automatisk styklisteforbrug.</span><span class="sxs-lookup"><span data-stu-id="dad2e-127">In the Automatic BOM consumption field, select 'Never'.</span></span>
12. <span data-ttu-id="dad2e-128">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="dad2e-128">Click OK.</span></span>
13. <span data-ttu-id="dad2e-129">Klik på Færdigmeld.</span><span class="sxs-lookup"><span data-stu-id="dad2e-129">Click Report as finished.</span></span>
14. <span data-ttu-id="dad2e-130">Klik på fanen Generelt.</span><span class="sxs-lookup"><span data-stu-id="dad2e-130">Click the General tab.</span></span>
15. <span data-ttu-id="dad2e-131">Vælg Ja i feltet Accepter fejl.</span><span class="sxs-lookup"><span data-stu-id="dad2e-131">Select Yes in the Accept error field.</span></span>
16. <span data-ttu-id="dad2e-132">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="dad2e-132">Click OK.</span></span>
17. <span data-ttu-id="dad2e-133">Klik på Lagersted i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="dad2e-133">On the Action Pane, click Warehouse.</span></span>
18. <span data-ttu-id="dad2e-134">Klik på Arbejdsdetaljer.</span><span class="sxs-lookup"><span data-stu-id="dad2e-134">Click Work details.</span></span>
    * <span data-ttu-id="dad2e-135">Når produktionsordren er færdigmeldt, oprettes der intet arbejde for læg-på-lager.</span><span class="sxs-lookup"><span data-stu-id="dad2e-135">When the production order was reported as finished, no work was generated for put-away.</span></span> <span data-ttu-id="dad2e-136">Dette skyldes, at der er defineret en arbejdspolitik, som forhindrer, at der genereres arbejde, når produktet L0101 rapporteres som færdigt på lokation 001.</span><span class="sxs-lookup"><span data-stu-id="dad2e-136">This occurs because a work policy is defined that prevents work from being generated when product L0101 is reported as finished to location 001.</span></span>  

