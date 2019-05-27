---
title: Konfigurere overførselsdokumenter for varebevægelser inden for et firma
description: Denne fremgangsmåde viser, hvordan du opretter dokumenter til flytning af varer i en virksomhed.
author: v-oloski
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTransferOrders, InventLocationIdLookup, TransportationDocument, HcmWorkerLookUp, SrsReportViewerForm, InventTransferParmShip
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 69542df1384bb36d89e2df5e5bc5fbe3dbe3c4cf
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1565014"
---
# <a name="set-up-the-transfer-documents-for-goods-movement-inside-a-company"></a><span data-ttu-id="0e27b-103">Konfigurere overførselsdokumenter for varebevægelser inden for et firma</span><span class="sxs-lookup"><span data-stu-id="0e27b-103">Set up the transfer documents for goods movement inside a company</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0e27b-104">Denne fremgangsmåde viser, hvordan du opretter dokumenter til flytning af varer i en virksomhed.</span><span class="sxs-lookup"><span data-stu-id="0e27b-104">This procedure shows how to create transfer documents for goods movement inside a company.</span></span> <span data-ttu-id="0e27b-105">Denne procedure er kun tilgængelig for juridiske enheder med en primær adresse i Litauen.</span><span class="sxs-lookup"><span data-stu-id="0e27b-105">This procedure is only available for legal entities with a primary address in Lithuania.</span></span> <span data-ttu-id="0e27b-106">Denne procedure blev oprettet ved hjælp af demodatafirmaet DEMF med primær adresse i Litauen.</span><span class="sxs-lookup"><span data-stu-id="0e27b-106">The procedure was created using the demo data company DEMF with a primary address in Lithuania.</span></span> <span data-ttu-id="0e27b-107">Før du kan udføre denne procedure, skal du fuldføre proceduren "Konfiguration af overførselsdokumenter for transport af varer inden for virksomheden".</span><span class="sxs-lookup"><span data-stu-id="0e27b-107">Before you can complete this procedure, you must complete the “Set up transfer documents for goods movement inside a company” procedure.</span></span> <span data-ttu-id="0e27b-108">Denne procedure er kun beregnet til lagerregnskabsmedarbejdere.</span><span class="sxs-lookup"><span data-stu-id="0e27b-108">This procedure is intended for inventory accountants.</span></span> <span data-ttu-id="0e27b-109">Denne procedure er beregnet til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.</span><span class="sxs-lookup"><span data-stu-id="0e27b-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-transfer-order"></a><span data-ttu-id="0e27b-110">Oprette en flytteordre</span><span class="sxs-lookup"><span data-stu-id="0e27b-110">Create a transfer order</span></span>
1. <span data-ttu-id="0e27b-111">Gå til Lagerstyring > Indgående ordrer > Overførselsordre.</span><span class="sxs-lookup"><span data-stu-id="0e27b-111">Go to Inventory management > Inbound orders > Transfer order.</span></span>
2. <span data-ttu-id="0e27b-112">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="0e27b-112">Click New.</span></span>
3. <span data-ttu-id="0e27b-113">Indtast eller vælg en værdi i feltet Fra lagersted.</span><span class="sxs-lookup"><span data-stu-id="0e27b-113">In the From warehouse field, enter or select a value.</span></span>
4. <span data-ttu-id="0e27b-114">Indtast eller vælg en værdi i feltet Til lagersted.</span><span class="sxs-lookup"><span data-stu-id="0e27b-114">In the To warehouse field, enter or select a value.</span></span>
5. <span data-ttu-id="0e27b-115">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="0e27b-115">Click Add.</span></span>
6. <span data-ttu-id="0e27b-116">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="0e27b-116">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="0e27b-117">Indtast eller vælg en værdi i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="0e27b-117">In the Item number field, enter or select a value.</span></span>

## <a name="enter-transportation-details-for-the-transfer-order"></a><span data-ttu-id="0e27b-118">Angiv transportdetaljer for flytteordren</span><span class="sxs-lookup"><span data-stu-id="0e27b-118">Enter transportation details for the transfer order</span></span>
1. <span data-ttu-id="0e27b-119">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="0e27b-119">Click Save.</span></span>
2. <span data-ttu-id="0e27b-120">Klik på Send i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="0e27b-120">On the Action Pane, click Ship.</span></span>
3. <span data-ttu-id="0e27b-121">Klik på Transportdetaljer.</span><span class="sxs-lookup"><span data-stu-id="0e27b-121">Click Transportation details.</span></span>
4. <span data-ttu-id="0e27b-122">Vælg Ja i feltet Udskriv transportdetaljer.</span><span class="sxs-lookup"><span data-stu-id="0e27b-122">Select Yes in the Print transportation details field.</span></span>
5. <span data-ttu-id="0e27b-123">Indtast eller vælg en værdi i feltet Afgang af varer udført af.</span><span class="sxs-lookup"><span data-stu-id="0e27b-123">In the Goods issued by field, enter or select a value.</span></span>
6. <span data-ttu-id="0e27b-124">Skriv en værdi i feltet Pakke.</span><span class="sxs-lookup"><span data-stu-id="0e27b-124">In the Package field, type a value.</span></span>
7. <span data-ttu-id="0e27b-125">Skriv en værdi i feltet Risikoniveau for indlæsning.</span><span class="sxs-lookup"><span data-stu-id="0e27b-125">In the Risk level of the load field, type a value.</span></span>
8. <span data-ttu-id="0e27b-126">Indtast eller vælg en værdi i feltet Fragtmand.</span><span class="sxs-lookup"><span data-stu-id="0e27b-126">In the Carrier field, enter or select a value.</span></span>
9. <span data-ttu-id="0e27b-127">Indtast eller vælg en værdi i feltet Model.</span><span class="sxs-lookup"><span data-stu-id="0e27b-127">In the Model field, enter or select a value.</span></span>
10. <span data-ttu-id="0e27b-128">Skriv en værdi i feltet Registreringsnummer.</span><span class="sxs-lookup"><span data-stu-id="0e27b-128">In the Registration number field, type a value.</span></span>
11. <span data-ttu-id="0e27b-129">Skriv en værdi i feltet Trailernummer.</span><span class="sxs-lookup"><span data-stu-id="0e27b-129">In the Trailer registration number field, type a value.</span></span>
12. <span data-ttu-id="0e27b-130">Indtast eller vælg en værdi i feltet Chauffør.</span><span class="sxs-lookup"><span data-stu-id="0e27b-130">In the Driver field, enter or select a value.</span></span>
13. <span data-ttu-id="0e27b-131">Angiv en værdi i feltet Chauffør.</span><span class="sxs-lookup"><span data-stu-id="0e27b-131">In the Driver name field, type a value.</span></span>
14. <span data-ttu-id="0e27b-132">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="0e27b-132">Click Save.</span></span>
15. <span data-ttu-id="0e27b-133">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0e27b-133">Close the page.</span></span>

## <a name="view-the-packing-slip-for-the-unposted-transfer-order"></a><span data-ttu-id="0e27b-134">Vis følgesedlen for den ikke-bogførte overførselsordre</span><span class="sxs-lookup"><span data-stu-id="0e27b-134">View the packing slip for the unposted transfer order</span></span>
1. <span data-ttu-id="0e27b-135">Klik på følgeseddel.</span><span class="sxs-lookup"><span data-stu-id="0e27b-135">Click Packing slip.</span></span>
2. <span data-ttu-id="0e27b-136">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0e27b-136">Click OK.</span></span>
3. <span data-ttu-id="0e27b-137">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0e27b-137">Close the page.</span></span>

## <a name="view-the-packing-slip-for-the-posted-transfer-order"></a><span data-ttu-id="0e27b-138">Vis følgesedlen for den bogførte overførselsordre</span><span class="sxs-lookup"><span data-stu-id="0e27b-138">View the packing slip for the posted transfer order</span></span>
1. <span data-ttu-id="0e27b-139">Klik på Overførselsordre i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="0e27b-139">On the Action Pane, click Transfer order.</span></span>
2. <span data-ttu-id="0e27b-140">Klik på Send i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="0e27b-140">On the Action Pane, click Ship.</span></span>
3. <span data-ttu-id="0e27b-141">Klik på Forsendelsesflytteordre.</span><span class="sxs-lookup"><span data-stu-id="0e27b-141">Click Ship transfer order.</span></span>
4. <span data-ttu-id="0e27b-142">Klik på fanen Generelt.</span><span class="sxs-lookup"><span data-stu-id="0e27b-142">Click the General tab.</span></span>
5. <span data-ttu-id="0e27b-143">Vælg en indstilling i feltet Opdater.</span><span class="sxs-lookup"><span data-stu-id="0e27b-143">In the Update field, select an option.</span></span>
6. <span data-ttu-id="0e27b-144">Klik på fanen Oversigt.</span><span class="sxs-lookup"><span data-stu-id="0e27b-144">Click the Overview tab.</span></span>
7. <span data-ttu-id="0e27b-145">Skriv en værdi i feltet Følgeseddel.</span><span class="sxs-lookup"><span data-stu-id="0e27b-145">In the Packing slip field, type a value.</span></span>
8. <span data-ttu-id="0e27b-146">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0e27b-146">Click OK.</span></span>
9. <span data-ttu-id="0e27b-147">Klik på Send i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="0e27b-147">On the Action Pane, click Ship.</span></span>
10. <span data-ttu-id="0e27b-148">Klik på følgeseddel.</span><span class="sxs-lookup"><span data-stu-id="0e27b-148">Click Packing slip.</span></span>
11. <span data-ttu-id="0e27b-149">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0e27b-149">Click OK.</span></span>

