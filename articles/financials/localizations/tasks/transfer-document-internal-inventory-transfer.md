---
title: Generere et overførselsdokument for en intern lageroverførsel
description: Denne fremgangsmåde viser, hvordan du opretter dokumenter til flytning af varer i en virksomhed.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTransferOrders, InventLocationIdLookup, TransportationDocument, HcmWorkerLookUp, SrsReportViewerForm, InventTransferParmShip
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a4da59781f3357a6713eebba03d87c5127b8cd3b
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/02/2019
ms.locfileid: "1848618"
---
# <a name="generate-a-transfer-document-for-an-internal-inventory-transfer"></a><span data-ttu-id="3f882-103">Generere et overførselsdokument for en intern lageroverførsel</span><span class="sxs-lookup"><span data-stu-id="3f882-103">Generate a transfer document for an internal inventory transfer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3f882-104">Denne fremgangsmåde viser, hvordan du opretter dokumenter til flytning af varer i en virksomhed.</span><span class="sxs-lookup"><span data-stu-id="3f882-104">This procedure shows how to create transfer documents for goods movement inside a company.</span></span> <span data-ttu-id="3f882-105">Denne procedure er kun tilgængelig for juridiske enheder med en primær adresse i Litauen.</span><span class="sxs-lookup"><span data-stu-id="3f882-105">This procedure is only available for legal entities with a primary address in Lithuania.</span></span> <span data-ttu-id="3f882-106">Denne procedure blev oprettet ved hjælp af demodatafirmaet DEMF med primær adresse i Litauen.</span><span class="sxs-lookup"><span data-stu-id="3f882-106">The procedure was created using the demo data company DEMF with a primary address in Lithuania.</span></span> <span data-ttu-id="3f882-107">Før du kan udføre denne procedure, skal du fuldføre proceduren "Konfiguration af overførselsdokumenter for transport af varer inden for virksomheden".</span><span class="sxs-lookup"><span data-stu-id="3f882-107">Before you can complete this procedure, you must complete the “Set up transfer documents for goods movement inside a company” procedure.</span></span> <span data-ttu-id="3f882-108">Denne procedure er kun beregnet til lagerregnskabsmedarbejdere.</span><span class="sxs-lookup"><span data-stu-id="3f882-108">This procedure is intended for inventory accountants.</span></span> <span data-ttu-id="3f882-109">Denne procedure er beregnet til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.</span><span class="sxs-lookup"><span data-stu-id="3f882-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-transfer-order"></a><span data-ttu-id="3f882-110">Oprette en flytteordre</span><span class="sxs-lookup"><span data-stu-id="3f882-110">Create a transfer order</span></span>
1. <span data-ttu-id="3f882-111">Gå til Lagerstyring > Indgående ordrer > Overførselsordre.</span><span class="sxs-lookup"><span data-stu-id="3f882-111">Go to Inventory management > Inbound orders > Transfer order.</span></span>
2. <span data-ttu-id="3f882-112">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="3f882-112">Click New.</span></span>
3. <span data-ttu-id="3f882-113">Indtast eller vælg en værdi i feltet Fra lagersted.</span><span class="sxs-lookup"><span data-stu-id="3f882-113">In the From warehouse field, enter or select a value.</span></span>
4. <span data-ttu-id="3f882-114">Indtast eller vælg en værdi i feltet Til lagersted.</span><span class="sxs-lookup"><span data-stu-id="3f882-114">In the To warehouse field, enter or select a value.</span></span>
5. <span data-ttu-id="3f882-115">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="3f882-115">Click Add.</span></span>
6. <span data-ttu-id="3f882-116">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="3f882-116">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="3f882-117">Indtast eller vælg en værdi i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="3f882-117">In the Item number field, enter or select a value.</span></span>

## <a name="enter-transportation-details-for-the-transfer-order"></a><span data-ttu-id="3f882-118">Angiv transportdetaljer for flytteordren</span><span class="sxs-lookup"><span data-stu-id="3f882-118">Enter transportation details for the transfer order</span></span>
1. <span data-ttu-id="3f882-119">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="3f882-119">Click Save.</span></span>
2. <span data-ttu-id="3f882-120">Klik på Send i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="3f882-120">On the Action Pane, click Ship.</span></span>
3. <span data-ttu-id="3f882-121">Klik på Transportdetaljer.</span><span class="sxs-lookup"><span data-stu-id="3f882-121">Click Transportation details.</span></span>
4. <span data-ttu-id="3f882-122">Vælg Ja i feltet Udskriv transportdetaljer.</span><span class="sxs-lookup"><span data-stu-id="3f882-122">Select Yes in the Print transportation details field.</span></span>
5. <span data-ttu-id="3f882-123">Indtast eller vælg en værdi i feltet Afgang af varer udført af.</span><span class="sxs-lookup"><span data-stu-id="3f882-123">In the Goods issued by field, enter or select a value.</span></span>
6. <span data-ttu-id="3f882-124">Skriv en værdi i feltet Pakke.</span><span class="sxs-lookup"><span data-stu-id="3f882-124">In the Package field, type a value.</span></span>
7. <span data-ttu-id="3f882-125">Skriv en værdi i feltet Risikoniveau for indlæsning.</span><span class="sxs-lookup"><span data-stu-id="3f882-125">In the Risk level of the load field, type a value.</span></span>
8. <span data-ttu-id="3f882-126">Indtast eller vælg en værdi i feltet Fragtmand.</span><span class="sxs-lookup"><span data-stu-id="3f882-126">In the Carrier field, enter or select a value.</span></span>
9. <span data-ttu-id="3f882-127">Indtast eller vælg en værdi i feltet Model.</span><span class="sxs-lookup"><span data-stu-id="3f882-127">In the Model field, enter or select a value.</span></span>
10. <span data-ttu-id="3f882-128">Skriv en værdi i feltet Registreringsnummer.</span><span class="sxs-lookup"><span data-stu-id="3f882-128">In the Registration number field, type a value.</span></span>
11. <span data-ttu-id="3f882-129">Skriv en værdi i feltet Trailernummer.</span><span class="sxs-lookup"><span data-stu-id="3f882-129">In the Trailer registration number field, type a value.</span></span>
12. <span data-ttu-id="3f882-130">Indtast eller vælg en værdi i feltet Chauffør.</span><span class="sxs-lookup"><span data-stu-id="3f882-130">In the Driver field, enter or select a value.</span></span>
13. <span data-ttu-id="3f882-131">Angiv en værdi i feltet Chauffør.</span><span class="sxs-lookup"><span data-stu-id="3f882-131">In the Driver name field, type a value.</span></span>
14. <span data-ttu-id="3f882-132">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="3f882-132">Click Save.</span></span>
15. <span data-ttu-id="3f882-133">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="3f882-133">Close the page.</span></span>

## <a name="view-the-packing-slip-for-the-unposted-transfer-order"></a><span data-ttu-id="3f882-134">Vis følgesedlen for den ikke-bogførte overførselsordre</span><span class="sxs-lookup"><span data-stu-id="3f882-134">View the packing slip for the unposted transfer order</span></span>
1. <span data-ttu-id="3f882-135">Klik på følgeseddel.</span><span class="sxs-lookup"><span data-stu-id="3f882-135">Click Packing slip.</span></span>
2. <span data-ttu-id="3f882-136">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="3f882-136">Click OK.</span></span>
3. <span data-ttu-id="3f882-137">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="3f882-137">Close the page.</span></span>

## <a name="view-the-packing-slip-for-the-posted-transfer-order"></a><span data-ttu-id="3f882-138">Vis følgesedlen for den bogførte overførselsordre</span><span class="sxs-lookup"><span data-stu-id="3f882-138">View the packing slip for the posted transfer order</span></span>
1. <span data-ttu-id="3f882-139">Klik på Overførselsordre i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="3f882-139">On the Action Pane, click Transfer order.</span></span>
2. <span data-ttu-id="3f882-140">Klik på Send i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="3f882-140">On the Action Pane, click Ship.</span></span>
3. <span data-ttu-id="3f882-141">Klik på Forsendelsesflytteordre.</span><span class="sxs-lookup"><span data-stu-id="3f882-141">Click Ship transfer order.</span></span>
4. <span data-ttu-id="3f882-142">Klik på fanen Generelt.</span><span class="sxs-lookup"><span data-stu-id="3f882-142">Click the General tab.</span></span>
5. <span data-ttu-id="3f882-143">Vælg en indstilling i feltet Opdater.</span><span class="sxs-lookup"><span data-stu-id="3f882-143">In the Update field, select an option.</span></span>
6. <span data-ttu-id="3f882-144">Klik på fanen Oversigt.</span><span class="sxs-lookup"><span data-stu-id="3f882-144">Click the Overview tab.</span></span>
7. <span data-ttu-id="3f882-145">Skriv en værdi i feltet Følgeseddel.</span><span class="sxs-lookup"><span data-stu-id="3f882-145">In the Packing slip field, type a value.</span></span>
8. <span data-ttu-id="3f882-146">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="3f882-146">Click OK.</span></span>
9. <span data-ttu-id="3f882-147">Klik på Send i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="3f882-147">On the Action Pane, click Ship.</span></span>
10. <span data-ttu-id="3f882-148">Klik på følgeseddel.</span><span class="sxs-lookup"><span data-stu-id="3f882-148">Click Packing slip.</span></span>
11. <span data-ttu-id="3f882-149">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="3f882-149">Click OK.</span></span>

