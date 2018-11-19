--- 
title: Konfigurere automatisk fragtafstemning
description: Denne procedure viser, hvordan du konfigurerer data til automatisk fragtafstemning.
author: ShylaThompson
manager: AnnBe
ms.date: 10/16/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TMSFreightBillType, TMSFreightBillTypeAssignment, TMSCarrierCodeLookup, DefaultDashboard, TMSAuditMaster
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d990efd7c929b15d57d64e850bc3308349abb978
ms.openlocfilehash: b7772ad779495b36941a3dc86cc456d80a964467
ms.contentlocale: da-dk
ms.lasthandoff: 10/17/2018

---
# <a name="set-up-automatic-freight-reconciliation"></a><span data-ttu-id="3cc77-103">Konfigurere automatisk fragtafstemning</span><span class="sxs-lookup"><span data-stu-id="3cc77-103">Set up automatic freight reconciliation</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3cc77-104">Denne procedure viser, hvordan du konfigurerer data til automatisk fragtafstemning.</span><span class="sxs-lookup"><span data-stu-id="3cc77-104">This procedure shows how to set up data for automatic freight reconciliation.</span></span> <span data-ttu-id="3cc77-105">Det udføres typisk af en lagerchef.</span><span class="sxs-lookup"><span data-stu-id="3cc77-105">This is typically done by a warehouse manager.</span></span> <span data-ttu-id="3cc77-106">Du kan bruge denne procedure i USMF-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="3cc77-106">You can use this procedure in demo data company USMF.</span></span>


## <a name="set-up-the-freight-bill-type"></a><span data-ttu-id="3cc77-107">Konfigurer fragtbrevstypen</span><span class="sxs-lookup"><span data-stu-id="3cc77-107">Set up the freight bill type</span></span>
1. <span data-ttu-id="3cc77-108">Gå til Transportstyring > Konfiguration > Afstemning af fragt > Fragtbrevstype.</span><span class="sxs-lookup"><span data-stu-id="3cc77-108">Go to Transportation management > Setup > Freight reconciliation > Freight bill type.</span></span>
    * <span data-ttu-id="3cc77-109">Typen af fragtbrev definerer, hvordan fragtbreve og fragtfakturaer skal sammenholdes.</span><span class="sxs-lookup"><span data-stu-id="3cc77-109">The freight bill type defines how freight bills and carrier invoices  should be matched.</span></span>  
2. <span data-ttu-id="3cc77-110">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="3cc77-110">Click New.</span></span>
3. <span data-ttu-id="3cc77-111">Skriv en værdi i feltet Fragtbrevstype.</span><span class="sxs-lookup"><span data-stu-id="3cc77-111">In the Freight bill type field, type a value.</span></span>
4. <span data-ttu-id="3cc77-112">I feltet Programassembly skal du skrive 'Microsoft.Dynamics.Ax.Tms.dll'.</span><span class="sxs-lookup"><span data-stu-id="3cc77-112">In the Engine assembly field, type 'Microsoft.Dynamics.Ax.Tms.dll'.</span></span>
    * <span data-ttu-id="3cc77-113">Dette er kodebiblioteket for programmet til sammenligning af transportstyring.</span><span class="sxs-lookup"><span data-stu-id="3cc77-113">This is the standard Transportation management matching engine code library.</span></span>  
5. <span data-ttu-id="3cc77-114">I feltet Programklasse skal du skrive 'Microsoft.Dynamics.Ax.Tms.Bll.GenericNormalizer'.</span><span class="sxs-lookup"><span data-stu-id="3cc77-114">In the Engine class field, type 'Microsoft.Dynamics.Ax.Tms.Bll.GenericNormalizer'.</span></span>
    * <span data-ttu-id="3cc77-115">Dette er klassen for programmet til sammenligning af transportstyring.</span><span class="sxs-lookup"><span data-stu-id="3cc77-115">This is the standard Transportation management matching engine class.</span></span>  
6. <span data-ttu-id="3cc77-116">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="3cc77-116">Click New.</span></span>
7. <span data-ttu-id="3cc77-117">Vælg den værdi, der skal svare til fragtbrevet og fragtfakturaen, i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="3cc77-117">In the Description field, choose the value that should match on the freight bill and the carrier invoice.</span></span>  
8. <span data-ttu-id="3cc77-118">Vælg 'Ja' i feltet Kræver afstemning.</span><span class="sxs-lookup"><span data-stu-id="3cc77-118">In the Match required field, select 'Yes'.</span></span>
    * <span data-ttu-id="3cc77-119">Hvis du angiver feltet til Ja, betyder det, at værdien i feltet Beskrivelse skal svare til både fragtbrevet og fragtfakturaen.</span><span class="sxs-lookup"><span data-stu-id="3cc77-119">If you set this field to Yes this means that the value selected in the Description field needs to match on both the freight bill and the carrier invoice.</span></span> <span data-ttu-id="3cc77-120">Hvis du angiver det til Nej, må feltet være tomt for en af disse.</span><span class="sxs-lookup"><span data-stu-id="3cc77-120">If you set it to No, the field can be blank on one of these.</span></span>  
9. <span data-ttu-id="3cc77-121">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="3cc77-121">Click Save.</span></span>

## <a name="set-up-the-freight-bill-type-assignment"></a><span data-ttu-id="3cc77-122">Konfigurer tildelingen af fragtbrevstype</span><span class="sxs-lookup"><span data-stu-id="3cc77-122">Set up the freight bill type assignment</span></span>
1. <span data-ttu-id="3cc77-123">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="3cc77-123">Close the page.</span></span>
2. <span data-ttu-id="3cc77-124">Gå til Transportstyring > Konfiguration > Afstemning af fragt > Tildelinger af fragtbrevstype.</span><span class="sxs-lookup"><span data-stu-id="3cc77-124">Go to Transportation management > Setup > Freight reconciliation > Freight bill type assignments.</span></span>
    * <span data-ttu-id="3cc77-125">Tildelingen af typen af fragtbrev bruges til at angive, hvilken type fragtbrev der bruges til en bestemt fragtmand.</span><span class="sxs-lookup"><span data-stu-id="3cc77-125">The freight bill type assignment is used to specify which freight bill type is used for a particular carrier.</span></span>   
3. <span data-ttu-id="3cc77-126">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="3cc77-126">Click New.</span></span>
4. <span data-ttu-id="3cc77-127">Indtast eller vælg en værdi i feltet Tilstand.</span><span class="sxs-lookup"><span data-stu-id="3cc77-127">In the Mode field, enter or select a value.</span></span>
5. <span data-ttu-id="3cc77-128">Indtast eller vælg en værdi i feltet Fragtmand.</span><span class="sxs-lookup"><span data-stu-id="3cc77-128">In the Shipping carrier field, enter or select a value.</span></span>
6. <span data-ttu-id="3cc77-129">Vælg typen fragtbrev, du oprettede tidligere, i feltet Fragtbrevstype.</span><span class="sxs-lookup"><span data-stu-id="3cc77-129">In the Freight bill type field, select the freight bill type that you created earlier.</span></span>
7. <span data-ttu-id="3cc77-130">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="3cc77-130">Close the page.</span></span>

## <a name="set-up-the-audit-master"></a><span data-ttu-id="3cc77-131">Konfigurer overvågningsmasteren</span><span class="sxs-lookup"><span data-stu-id="3cc77-131">Set up the audit master</span></span>
1. <span data-ttu-id="3cc77-132">Gå til Transportstyring > Konfiguration > Afstemning af fragt > Revisionsmaster.</span><span class="sxs-lookup"><span data-stu-id="3cc77-132">Go to Transportation management > Setup > Freight reconciliation > Audit master.</span></span>
    * <span data-ttu-id="3cc77-133">I revisionsmasteren defineres tolerancegrænserne for automatisk fragtafstemning.</span><span class="sxs-lookup"><span data-stu-id="3cc77-133">The audit master defines the tolerance limits for automatic freight reconciliation.</span></span> <span data-ttu-id="3cc77-134">Den angiver, hvor meget pengebeløbene i fragtbrevet og i fragtfakturaen kan variere og stadig tillade, at afstemningen finder sted.</span><span class="sxs-lookup"><span data-stu-id="3cc77-134">It specifies by how much the monetary amounts on the freight bill and the carrier invoice can differ and still allow reconciliation to occur.</span></span> <span data-ttu-id="3cc77-135">Den definerer også, hvordan du håndterer uoverensstemmelser.</span><span class="sxs-lookup"><span data-stu-id="3cc77-135">It also defines how to handle discrepancies.</span></span>  
2. <span data-ttu-id="3cc77-136">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="3cc77-136">Click New.</span></span>
3. <span data-ttu-id="3cc77-137">Skriv en værdi i feltet Revisionsmaster.</span><span class="sxs-lookup"><span data-stu-id="3cc77-137">In the Audit master ID field, type a value.</span></span>
4. <span data-ttu-id="3cc77-138">Vælg samme fragtmand som tidligere i feltet Fragtmand.</span><span class="sxs-lookup"><span data-stu-id="3cc77-138">In the Shipping carrier  field, select the same shipping carrier as you did earlier.</span></span>
5. <span data-ttu-id="3cc77-139">Vælg typen fragtbrev, du oprettede tidligere, i feltet Fragtbrevstype.</span><span class="sxs-lookup"><span data-stu-id="3cc77-139">In the Freight bill type field, select the freight bill type that you created earlier.</span></span>
6. <span data-ttu-id="3cc77-140">Udvid afsnittet Tolerance.</span><span class="sxs-lookup"><span data-stu-id="3cc77-140">Expand the Tolerance section.</span></span>
7. <span data-ttu-id="3cc77-141">Skriv et tal i feltet Min. toleranceniveau.</span><span class="sxs-lookup"><span data-stu-id="3cc77-141">In the Minimum tolerance level field, enter a number.</span></span>
8. <span data-ttu-id="3cc77-142">Skriv et tal i feltet Maks. toleranceniveau.</span><span class="sxs-lookup"><span data-stu-id="3cc77-142">In the Maximum tolerance level field, enter a number.</span></span>
9. <span data-ttu-id="3cc77-143">Udvid afsnittet Resultat.</span><span class="sxs-lookup"><span data-stu-id="3cc77-143">Expand the Result section.</span></span>
10. <span data-ttu-id="3cc77-144">Indtast eller vælg en værdi i feltet Årsagskode for overbetaling.</span><span class="sxs-lookup"><span data-stu-id="3cc77-144">In the Overpayment reason code field, enter or select a value.</span></span>
    * <span data-ttu-id="3cc77-145">Hvis pengebeløbene afviger i fragtbrevet og fragtfakturaen, angiver årsagskoderne for overbetaling eller underbetaling de konti, som forskellen skal registreres på, så længe forskellen ligger inden for toleranceniveauerne.</span><span class="sxs-lookup"><span data-stu-id="3cc77-145">If the monetary amounts differ on the freight bill and the carrier invoice, the overpayment and underpayment reason codes specify the accounts that the difference should be registered on, as long as the difference is within the tolerance levels.</span></span>  
11. <span data-ttu-id="3cc77-146">Indtast eller vælg en værdi i feltet Årsagskode for underbetaling.</span><span class="sxs-lookup"><span data-stu-id="3cc77-146">In the Underpayment reason code field, enter or select a value.</span></span>
12. <span data-ttu-id="3cc77-147">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="3cc77-147">Close the page.</span></span>


