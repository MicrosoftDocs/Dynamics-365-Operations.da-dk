---
title: Frigive produktionsordrer
description: En frigivet produktionsordre er en ordre, der er godkendt til produktion. Udtrykket Frigivet bruges til at beskrive en tilstand i produktionsordrens levetid, hvor produktionsordren er tilgængelig til udførelse på produktionen og lagerprocesser.
author: johanhoffmann
ms.date: 03/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProdParmRelease
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2414
ms.assetid: 50c2257b-2924-44f5-b7c1-11f498092053
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 118b0d6300647135b22e42cc84a79f07e48d7ef4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811696"
---
# <a name="release-production-orders"></a><span data-ttu-id="f6ffb-104">Frigive produktionsordrer</span><span class="sxs-lookup"><span data-stu-id="f6ffb-104">Release production orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f6ffb-105">En frigivet produktionsordre er en ordre, der er godkendt til produktion.</span><span class="sxs-lookup"><span data-stu-id="f6ffb-105">A released production order is an order that has been authorized for production.</span></span> <span data-ttu-id="f6ffb-106">Udtrykket Frigivet bruges til at beskrive en tilstand i produktionsordrens levetid, hvor produktionsordren er tilgængelig til udførelse på produktionen og lagerprocesser.</span><span class="sxs-lookup"><span data-stu-id="f6ffb-106">The term Released is used to describe a state in the production order life cycle, where the production order is available for execution on the production shop floor and for warehouse processes.</span></span>

## <a name="characteristics-of-the-released-state"></a><span data-ttu-id="f6ffb-107">Egenskaber for tilstanden Frigivet</span><span class="sxs-lookup"><span data-stu-id="f6ffb-107">Characteristics of the Released state</span></span>

<span data-ttu-id="f6ffb-108">Tilstanden **Frigivet** er en af tilstandene i produktionsordrens levetid.</span><span class="sxs-lookup"><span data-stu-id="f6ffb-108">The **Released** state is one state in the production order life cycle.</span></span> <span data-ttu-id="f6ffb-109">Produktionsordrer, der er i tilstanden **Frigivet**, er tilgængelige til udførelse i produktionen og for lagerprocesser.</span><span class="sxs-lookup"><span data-stu-id="f6ffb-109">Production orders that are in the **Released** state are available for execution on the production shop floor and for warehouse processes.</span></span> <span data-ttu-id="f6ffb-110">Tilstanden **Frigivet** har følgende egenskaber:</span><span class="sxs-lookup"><span data-stu-id="f6ffb-110">The **Released** state has the following characteristics:</span></span>

- <span data-ttu-id="f6ffb-111">En produktionsordre kan ændres til tilstanden **Frigivet** fra produktionsordren eller ved hjælp af en batchproces.</span><span class="sxs-lookup"><span data-stu-id="f6ffb-111">A production order can be changed to the **Released** state either from the production order or by using a batch process.</span></span> <span data-ttu-id="f6ffb-112">Produktionsordren kan også opdateres automatisk fra produktionsordreforslaget, der er autoriseret ved hjælp af feltet **Autorisationstidshorisont** på siden **Behovsplan**.</span><span class="sxs-lookup"><span data-stu-id="f6ffb-112">The production order can also be updated automatically from planned production orders that are firmed by using the **Firming time fence** field on the **Master plan** page.</span></span>
- <span data-ttu-id="f6ffb-113">Tilstanden **Frigivet** er signalet til produktionen (operatører) om at starte produktionsjob i produktionen.</span><span class="sxs-lookup"><span data-stu-id="f6ffb-113">The **Released** state is the signal for the shop floor operators (operators) to start executing the production jobs on the shop floor.</span></span>
- <span data-ttu-id="f6ffb-114">Produktionspapirer som rutekort, rutejob og jobkort indeholder oplysninger om produktionsjob og kan udstedes.</span><span class="sxs-lookup"><span data-stu-id="f6ffb-114">Production papers, such as route cards, route jobs, and jobs cards provide information about production jobs and can be issued.</span></span>
- <span data-ttu-id="f6ffb-115">I forbindelse med materialer, der er fysisk reserveret, genereres lagerarbejde til at plukke materialer til produktionsordren.</span><span class="sxs-lookup"><span data-stu-id="f6ffb-115">For materials that are physically reserved, warehouse work is generated to pick materials for the production order.</span></span>

## <a name="releasing-jobs-to-the-shop-floor"></a><span data-ttu-id="f6ffb-116">Frigive job til produktionen</span><span class="sxs-lookup"><span data-stu-id="f6ffb-116">Releasing jobs to the shop floor</span></span>

<span data-ttu-id="f6ffb-117">Når en produktionsordre er blevet frigivet, er produktionsjob, der vedrører ordren, synlige og klar til registrering.</span><span class="sxs-lookup"><span data-stu-id="f6ffb-117">After a production order is released, production jobs that are related to the order are visible and ready for registration.</span></span> <span data-ttu-id="f6ffb-118">Operatørerne kan foretage jobregistreringer, f.eks. Start, Stop og Færdiggørelse på enten siden **Jobkortsterminal** eller siden **Jobkortenhed**.</span><span class="sxs-lookup"><span data-stu-id="f6ffb-118">The operators can make job registrations, such as Start, Stop, and Completion, on either the **Job card terminal** page or the **Job card device** page.</span></span> <span data-ttu-id="f6ffb-119">Den registrerede tid og det registrerede antal overføres automatisk fra registreringssiderne til produktionskladder for at holde styr på den forbrugte tid og det forbrugte antal.</span><span class="sxs-lookup"><span data-stu-id="f6ffb-119">The registered time and quantity are automatically transferred from the registration pages to production journals to keep track of the consumed time and quantity.</span></span>

## <a name="route-cards"></a><span data-ttu-id="f6ffb-120">Rutekort</span><span class="sxs-lookup"><span data-stu-id="f6ffb-120">Route cards</span></span>

<span data-ttu-id="f6ffb-121">Et rutekort giver en oversigt over oplysninger, der stammer fra opsætninger af rute og operation og fra metoder til grovplanlægning og finplanlægning.</span><span class="sxs-lookup"><span data-stu-id="f6ffb-121">A route card provides an overview of information that comes from route and operation setups, and from operation and job scheduling methods.</span></span>

## <a name="route-jobs"></a><span data-ttu-id="f6ffb-122">Rutejob</span><span class="sxs-lookup"><span data-stu-id="f6ffb-122">Route jobs</span></span>

<span data-ttu-id="f6ffb-123">Et jobkort viser hvert job for en handling i detaljer og omfatter opsætning, proces, kø og transporttider.</span><span class="sxs-lookup"><span data-stu-id="f6ffb-123">A route job lists each job of an operation in detail, and includes setup, process, queue, and transportation times.</span></span> <span data-ttu-id="f6ffb-124">En handling, f.eks maling, kan kræve individuelle job som installationstid, køretid til maleprocessen og køtid til tørring.</span><span class="sxs-lookup"><span data-stu-id="f6ffb-124">For example, an operation such as painting might require individual jobs, such as setup time, run time for the painting process, and queue time for drying.</span></span>

## <a name="job-cards"></a><span data-ttu-id="f6ffb-125">Jobkort</span><span class="sxs-lookup"><span data-stu-id="f6ffb-125">Job cards</span></span>

<span data-ttu-id="f6ffb-126">Et jobkort viser de enkelte jobnumre for en bestemt handling.</span><span class="sxs-lookup"><span data-stu-id="f6ffb-126">A job card lists the individual job numbers of a particular operation.</span></span> <span data-ttu-id="f6ffb-127">Der vises et job på hver side.</span><span class="sxs-lookup"><span data-stu-id="f6ffb-127">One job appears on each page.</span></span> <span data-ttu-id="f6ffb-128">De job, der findes på et jobkort, og deres forventede tidspunkter stammer fra opsætningsoplysninger om rute og drift.</span><span class="sxs-lookup"><span data-stu-id="f6ffb-128">The jobs that are included on a job card, and their estimated times, come from the route and operation setup information.</span></span> <span data-ttu-id="f6ffb-129">Fra et jobkort kan du åbne siden **Produktionskladdelinjer**, **jobkort**.</span><span class="sxs-lookup"><span data-stu-id="f6ffb-129">From a job card, you can open the **Production journal lines**, **job card** page.</span></span> <span data-ttu-id="f6ffb-130">De personer, der kører operationsressourcer, kan give tilbagemeldinger om produktionsprocessen.</span><span class="sxs-lookup"><span data-stu-id="f6ffb-130">People who run operations resources can provide feedback about the production process.</span></span> <span data-ttu-id="f6ffb-131">Der er felter, hvor du kan angive forbrugsstatistikker og oplysninger som f.eks antallet af fejl.</span><span class="sxs-lookup"><span data-stu-id="f6ffb-131">There are fields where you can enter consumption statistics and information such as the error quantity.</span></span>

## <a name="warehouse-work-for-raw-material-picking"></a><span data-ttu-id="f6ffb-132">Lagersted for pluk af råvarer</span><span class="sxs-lookup"><span data-stu-id="f6ffb-132">Warehouse work for raw material picking</span></span>

<span data-ttu-id="f6ffb-133">Arbejde til pluk af råvarer genereres under frigivelse.</span><span class="sxs-lookup"><span data-stu-id="f6ffb-133">Work for raw material picking is generated during release.</span></span> <span data-ttu-id="f6ffb-134">Arbejde oprettes kun for den mængde materialer, der var fysisk reserveret til produktionsordren, før ordren blev frigivet.</span><span class="sxs-lookup"><span data-stu-id="f6ffb-134">Work is generated only for the quantity of materials that was physically reserved for the production order before the order was released.</span></span> <span data-ttu-id="f6ffb-135">Der kræves følgende opsætning for at generere lagerstedsarbejde til råvarepluk:</span><span class="sxs-lookup"><span data-stu-id="f6ffb-135">The following setup is required to generate warehouse work for raw material picking:</span></span>

- <span data-ttu-id="f6ffb-136">En bestemmelse for placering for pluk af råvarer, som bestemmer, hvilken lagerlokalitet materialerne skal plukkes i</span><span class="sxs-lookup"><span data-stu-id="f6ffb-136">A location directive for raw materials picking that determines which warehouse location to pick the materials in</span></span>
- <span data-ttu-id="f6ffb-137">En bølgeskabelon for råvarer, hvor politikkerne for udførelse af lagerarbejde konfigureres</span><span class="sxs-lookup"><span data-stu-id="f6ffb-137">A wave template for raw materials, where policies for the execution of warehouse work are configured</span></span>
- <span data-ttu-id="f6ffb-138">En indlagringslokation for produktion, der bestemmer, hvor materialer lægges på lager</span><span class="sxs-lookup"><span data-stu-id="f6ffb-138">A production input location that determines where materials are put</span></span>

<span data-ttu-id="f6ffb-139">Ved brug af lokationer, der styres af nummerplader, kan du vælge, om det bestilte antal eller det fulde antal, der er til rådighed for varen, skal plukkes under behandlingen af plukarbejdet med råmaterialerne.</span><span class="sxs-lookup"><span data-stu-id="f6ffb-139">When using license plate controlled locations, you can choose whether the ordered quantity or the full quantity available for the item should be picked while processing the raw material picking work.</span></span> <span data-ttu-id="f6ffb-140">Sådan angiver du dette:</span><span class="sxs-lookup"><span data-stu-id="f6ffb-140">To set this option:</span></span>

1. <span data-ttu-id="f6ffb-141">Gå til **Administration af produktoplysninger \> Produkter \> Frigivne produkter**, og åbn den relevante vare.</span><span class="sxs-lookup"><span data-stu-id="f6ffb-141">Go to **Product information management \> Products \> Released products** and open the relevant item.</span></span>
1. <span data-ttu-id="f6ffb-142">Udvid oversigtspanelet **Lagersted**.</span><span class="sxs-lookup"><span data-stu-id="f6ffb-142">Expand the **Warehouse** FastTab.</span></span>
1. <span data-ttu-id="f6ffb-143">Vælg en af følgende indstillinger for feltet **Materialepluk i nummerpladelokationer**:</span><span class="sxs-lookup"><span data-stu-id="f6ffb-143">Select one of the following options for the  **Material picking in license plate locations** field:</span></span>
    - <span data-ttu-id="f6ffb-144">*Ordrepluk*: Kun det bestilte antal skal plukkes.</span><span class="sxs-lookup"><span data-stu-id="f6ffb-144">*Order picking*: Only the ordered quantity should be picked.</span></span>
    - <span data-ttu-id="f6ffb-145">*Midlertidig* Når det er muligt, skal hele det disponible antal plukkes fra nummerpladen.</span><span class="sxs-lookup"><span data-stu-id="f6ffb-145">*Staging*: Whenever possible, the full quantity available at the license plate should be picked.</span></span> <span data-ttu-id="f6ffb-146">Hvis en arbejder skal kunne plukke hele nummerpladeantallet, må nummerpladen ikke indeholde blandede varer og må ikke have blandede dimensioner.</span><span class="sxs-lookup"><span data-stu-id="f6ffb-146">For a worker to be able to pick the full license plate quantity, the license plate must not contain mixed items and must not have mixed dimensions.</span></span> <span data-ttu-id="f6ffb-147">Hvis nummerpladen indeholder blandede dimensioner eller varer, fortsætter plukningen, som om den var indstillet til *Ordrepluk*.</span><span class="sxs-lookup"><span data-stu-id="f6ffb-147">If the license plate contains mixed dimensions or items, the pick will proceed as if it were set to *Order picking*.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]