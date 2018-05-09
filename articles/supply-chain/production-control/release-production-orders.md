---
title: Frigive produktionsordrer
description: "En frigivet produktionsordre er en ordre, der er godkendt til produktion. Udtrykket Frigivet bruges til at beskrive en tilstand i produktionsordrens levetid, hvor produktionsordren er tilgængelig til udførelse på produktionen og lagerprocesser."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdParmRelease
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 2414
ms.assetid: 50c2257b-2924-44f5-b7c1-11f498092053
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: e0e7f3747980ff2fb5d055c9496167888e067f8d
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---

# <a name="release-production-orders"></a><span data-ttu-id="0e512-104">Frigive produktionsordrer</span><span class="sxs-lookup"><span data-stu-id="0e512-104">Release production orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0e512-105">En frigivet produktionsordre er en ordre, der er godkendt til produktion.</span><span class="sxs-lookup"><span data-stu-id="0e512-105">A released production order is an order that has been authorized for production.</span></span> <span data-ttu-id="0e512-106">Udtrykket Frigivet bruges til at beskrive en tilstand i produktionsordrens levetid, hvor produktionsordren er tilgængelig til udførelse på produktionen og lagerprocesser.</span><span class="sxs-lookup"><span data-stu-id="0e512-106">The term Released is used to describe a state in the production order life cycle, where the production order is available for execution on the production shop floor and for warehouse processes.</span></span> 

<a name="characteristics-of-the-released-state"></a><span data-ttu-id="0e512-107">Egenskaber for tilstanden Frigivet</span><span class="sxs-lookup"><span data-stu-id="0e512-107">Characteristics of the Released state</span></span>
-------------------------------------

<span data-ttu-id="0e512-108">Tilstanden **Frigivet** er en af tilstandene i produktionsordrens levetid.</span><span class="sxs-lookup"><span data-stu-id="0e512-108">The **Released** state is one state in the production order life cycle.</span></span> <span data-ttu-id="0e512-109">Produktionsordrer, der er i tilstanden **Frigivet**, er tilgængelige til udførelse i produktionen og for lagerprocesser.</span><span class="sxs-lookup"><span data-stu-id="0e512-109">Production orders that are in the **Released** state are available for execution on the production shop floor and for warehouse processes.</span></span> <span data-ttu-id="0e512-110">Tilstanden **Frigivet** har følgende egenskaber:</span><span class="sxs-lookup"><span data-stu-id="0e512-110">The **Released** state has the following characteristics:</span></span>

-   <span data-ttu-id="0e512-111">En produktionsordre kan ændres til tilstanden **Frigivet** fra produktionsordren eller ved hjælp af en batchproces.</span><span class="sxs-lookup"><span data-stu-id="0e512-111">A production order can be changed to the **Released** state either from the production order or by using a batch process.</span></span> <span data-ttu-id="0e512-112">Produktionsordren kan også opdateres automatisk fra produktionsordreforslaget, der er autoriseret ved hjælp af feltet **Autorisationstidshorisont** på siden **Behovsplan**.</span><span class="sxs-lookup"><span data-stu-id="0e512-112">The production order can also be updated automatically from planned production orders that are firmed by using the **Firming time fence** field on the **Master plan** page.</span></span>
-   <span data-ttu-id="0e512-113">Tilstanden **Frigivet** er signalet til produktionen (operatører) om at starte produktionsjob i produktionen.</span><span class="sxs-lookup"><span data-stu-id="0e512-113">The **Released** state is the signal for the shop floor operators (operators) to start executing the production jobs on the shop floor.</span></span>
-   <span data-ttu-id="0e512-114">Produktionspapirer som rutekort, rutejob og jobkort indeholder oplysninger om produktionsjob og kan udstedes.</span><span class="sxs-lookup"><span data-stu-id="0e512-114">Production papers, such as route cards, route jobs, and jobs cards provide information about production jobs and can be issued.</span></span>
-   <span data-ttu-id="0e512-115">I forbindelse med materialer, der er fysisk reserveret, genereres lagerarbejde til at plukke materialer til produktionsordren.</span><span class="sxs-lookup"><span data-stu-id="0e512-115">For materials that are physically reserved, warehouse work is generated to pick materials for the production order.</span></span>

## <a name="releasing-jobs-to-the-shop-floor"></a><span data-ttu-id="0e512-116">Frigive job til produktionen</span><span class="sxs-lookup"><span data-stu-id="0e512-116">Releasing jobs to the shop floor</span></span>
<span data-ttu-id="0e512-117">Når en produktionsordre er blevet frigivet, er produktionsjob, der vedrører ordren, synlige og klar til registrering.</span><span class="sxs-lookup"><span data-stu-id="0e512-117">After a production order is released, production jobs that are related to the order are visible and ready for registration.</span></span> <span data-ttu-id="0e512-118">Operatørerne kan foretage jobregistreringer, f.eks. Start, Stop og Færdiggørelse på enten siden **Jobkortsterminal** eller siden **Jobkortenhed**.</span><span class="sxs-lookup"><span data-stu-id="0e512-118">The operators can make job registrations, such as Start, Stop, and Completion, on either the **Job card terminal** page or the **Job card device** page.</span></span> <span data-ttu-id="0e512-119">Den registrerede tid og det registrerede antal overføres automatisk fra registreringssiderne til produktionskladder for at holde styr på den forbrugte tid og det forbrugte antal.</span><span class="sxs-lookup"><span data-stu-id="0e512-119">The registered time and quantity are automatically transferred from the registration pages to production journals to keep track of the consumed time and quantity.</span></span>

## <a name="route-cards"></a><span data-ttu-id="0e512-120">Rutekort</span><span class="sxs-lookup"><span data-stu-id="0e512-120">Route cards</span></span>
<span data-ttu-id="0e512-121">Et rutekort giver en oversigt over oplysninger, der stammer fra opsætninger af rute og operation og fra metoder til grovplanlægning og finplanlægning.</span><span class="sxs-lookup"><span data-stu-id="0e512-121">A route card provides an overview of information that comes from route and operation setups, and from operation and job scheduling methods.</span></span>

## <a name="route-jobs"></a><span data-ttu-id="0e512-122">Rutejob</span><span class="sxs-lookup"><span data-stu-id="0e512-122">Route jobs</span></span>
<span data-ttu-id="0e512-123">Et jobkort viser hvert job for en handling i detaljer og omfatter opsætning, proces, kø og transporttider.</span><span class="sxs-lookup"><span data-stu-id="0e512-123">A route job lists each job of an operation in detail, and includes setup, process, queue, and transportation times.</span></span> <span data-ttu-id="0e512-124">En handling, f.eks maling, kan kræve individuelle job som installationstid, køretid til maleprocessen og køtid til tørring.</span><span class="sxs-lookup"><span data-stu-id="0e512-124">For example, an operation such as painting might require individual jobs, such as setup time, run time for the painting process, and queue time for drying.</span></span>

## <a name="job-cards"></a><span data-ttu-id="0e512-125">Jobkort</span><span class="sxs-lookup"><span data-stu-id="0e512-125">Job cards</span></span>
<span data-ttu-id="0e512-126">Et jobkort viser de enkelte jobnumre for en bestemt handling.</span><span class="sxs-lookup"><span data-stu-id="0e512-126">A job card lists the individual job numbers of a particular operation.</span></span> <span data-ttu-id="0e512-127">Der vises et job på hver side.</span><span class="sxs-lookup"><span data-stu-id="0e512-127">One job appears on each page.</span></span> <span data-ttu-id="0e512-128">De job, der findes på et jobkort, og deres forventede tidspunkter stammer fra opsætningsoplysninger om rute og drift.</span><span class="sxs-lookup"><span data-stu-id="0e512-128">The jobs that are included on a job card, and their estimated times, come from the route and operation setup information.</span></span> <span data-ttu-id="0e512-129">Fra et jobkort kan du åbne siden **Produktionskladdelinjer**, **jobkort**.</span><span class="sxs-lookup"><span data-stu-id="0e512-129">From a job card, you can open the **Production journal lines**, **job card** page.</span></span> <span data-ttu-id="0e512-130">De personer, der kører operationsressourcer, kan give tilbagemeldinger om produktionsprocessen.</span><span class="sxs-lookup"><span data-stu-id="0e512-130">People who run operations resources can provide feedback about the production process.</span></span> <span data-ttu-id="0e512-131">Der er felter, hvor du kan angive forbrugsstatistikker og oplysninger som f.eks antallet af fejl.</span><span class="sxs-lookup"><span data-stu-id="0e512-131">There are fields where you can enter consumption statistics and information such as the error quantity.</span></span>

## <a name="warehouse-work-for-raw-material-picking"></a><span data-ttu-id="0e512-132">Lagersted for pluk af råvarer</span><span class="sxs-lookup"><span data-stu-id="0e512-132">Warehouse work for raw material picking</span></span>
<span data-ttu-id="0e512-133">Arbejde til pluk af råvarer genereres under frigivelse.</span><span class="sxs-lookup"><span data-stu-id="0e512-133">Work for raw material picking is generated during release.</span></span> <span data-ttu-id="0e512-134">Arbejde oprettes kun for den mængde materialer, der var fysisk reserveret til produktionsordren, før ordren blev frigivet.</span><span class="sxs-lookup"><span data-stu-id="0e512-134">Work is generated only for the quantity of materials that was physically reserved for the production order before the order was released.</span></span> <span data-ttu-id="0e512-135">Der kræves følgende opsætning for at generere lagerstedsarbejde til råvarepluk:</span><span class="sxs-lookup"><span data-stu-id="0e512-135">The following setup is required to generate warehouse work for raw material picking:</span></span>

-   <span data-ttu-id="0e512-136">En bestemmelse for placering for pluk af råvarer, som bestemmer, hvilken lagerlokalitet materialerne skal plukkes i</span><span class="sxs-lookup"><span data-stu-id="0e512-136">A location directive for raw materials picking that determines which warehouse location to pick the materials in</span></span>
-   <span data-ttu-id="0e512-137">En bølgeskabelon for råvarer, hvor politikkerne for udførelse af lagerarbejde konfigureres</span><span class="sxs-lookup"><span data-stu-id="0e512-137">A wave template for raw materials, where policies for the execution of warehouse work are configured</span></span>
-   <span data-ttu-id="0e512-138">En indlagringslokation for produktion, der bestemmer, hvor materialer lægges på lager</span><span class="sxs-lookup"><span data-stu-id="0e512-138">A production input location that determines where materials are put</span></span>





