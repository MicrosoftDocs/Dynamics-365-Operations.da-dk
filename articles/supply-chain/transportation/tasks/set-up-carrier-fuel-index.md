--- 
title: "Konfigurere et brændstofindeks for fragtmand"
description: "Denne vejledning viser, hvordan du opretter et område for brændstofindeks, et brændstofindeks og fragtmandens brændstofindeks."
author: BibiSp
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: cd9842a14d512353bda399a9d83eb7296a75d982
ms.contentlocale: da-dk
ms.lasthandoff: 04/13/2018

---
# <a name="set-up-a-carrier-fuel-index"></a><span data-ttu-id="2e82b-103">Konfigurere et brændstofindeks for fragtmand</span><span class="sxs-lookup"><span data-stu-id="2e82b-103">Set up a carrier fuel index</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2e82b-104">Denne vejledning viser, hvordan du opretter et område for brændstofindeks, et brændstofindeks og fragtmandens brændstofindeks.</span><span class="sxs-lookup"><span data-stu-id="2e82b-104">This guide shows how to create a fuel index region, a fuel index and a carrier fuel index.</span></span> <span data-ttu-id="2e82b-105">Området for brændstofindeks angiver hvilket område brændstofindekset skal gælde for, og brændstofindekset angiver en brændstofpris for en bestemt tidsperiode.</span><span class="sxs-lookup"><span data-stu-id="2e82b-105">The fuel index region specifies which region the fuel index should apply to, and the fuel index specifies a fuel price for a particular period of time.</span></span> <span data-ttu-id="2e82b-106">For at afspejle ændringer i brændstofpriser over tid kan du knytte flere brændstofindekser til en fragtmand.</span><span class="sxs-lookup"><span data-stu-id="2e82b-106">To reflect the change in fuel prices over time, you can associate multiple fuel indexes with a carrier.</span></span>  <span data-ttu-id="2e82b-107">Disse opgaver udføres normalt af en transportkoordinator.</span><span class="sxs-lookup"><span data-stu-id="2e82b-107">These tasks are normally done by a transportation coordinator.</span></span> <span data-ttu-id="2e82b-108">Du kan bruge denne procedure i USMF-demodatafirmaet eller ved at bruge dine egne data.</span><span class="sxs-lookup"><span data-stu-id="2e82b-108">You can use this procedure in demo data company USMF or using your own data.</span></span>


## <a name="create-a-fuel-index-region"></a><span data-ttu-id="2e82b-109">Opret et område for brændstofindeks</span><span class="sxs-lookup"><span data-stu-id="2e82b-109">Create a fuel index region</span></span>
1. <span data-ttu-id="2e82b-110">Gå til Transportstyring > Opsætning > Brændstofindekser > Områder for brændstofindeks.</span><span class="sxs-lookup"><span data-stu-id="2e82b-110">Go to Transportation management > Setup > Fuel indexes > Fuel index regions.</span></span>
    * <span data-ttu-id="2e82b-111">Først er det nødvendigt at oprette forskellige områder, hvor du bruger og beregner forskellige brændstoftillæg.</span><span class="sxs-lookup"><span data-stu-id="2e82b-111">First you have to create the different regions, where you operate and calculate different fuel surcharges.</span></span>  
2. <span data-ttu-id="2e82b-112">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="2e82b-112">Click New.</span></span>
3. <span data-ttu-id="2e82b-113">Skriv en værdi i feltet Område.</span><span class="sxs-lookup"><span data-stu-id="2e82b-113">In the Region field, type a value.</span></span>
4. <span data-ttu-id="2e82b-114">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="2e82b-114">In the Name field, type a value.</span></span>
5. <span data-ttu-id="2e82b-115">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="2e82b-115">Click Save.</span></span>

## <a name="create-a-fuel-index"></a><span data-ttu-id="2e82b-116">Oprette et brændstofindeks</span><span class="sxs-lookup"><span data-stu-id="2e82b-116">Create a fuel index</span></span>
1. <span data-ttu-id="2e82b-117">Gå til Transportstyring > Opsætning > Brændstofindekser > Brændstofindekser.</span><span class="sxs-lookup"><span data-stu-id="2e82b-117">Go to Transportation management > Setup > Fuel indexes > Fuel indexes.</span></span>
    * <span data-ttu-id="2e82b-118">Du skal angive de aktuelle priser for brændstof for de områder, du har oprettet.</span><span class="sxs-lookup"><span data-stu-id="2e82b-118">For the regions you have set up you need to enter the current prices for the fuel.</span></span>  
2. <span data-ttu-id="2e82b-119">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="2e82b-119">Click New.</span></span>
3. <span data-ttu-id="2e82b-120">Klik på rullelisten i feltet Område for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="2e82b-120">In the Region field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="2e82b-121">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="2e82b-121">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="2e82b-122">Angiv et tal i feltet Pris pr. gallon.</span><span class="sxs-lookup"><span data-stu-id="2e82b-122">In the Price per gallon field, enter a number.</span></span>
6. <span data-ttu-id="2e82b-123">Angiv en dato og et klokkeslæt i feltet Gældende startdato og -klokkeslæt.</span><span class="sxs-lookup"><span data-stu-id="2e82b-123">In the Effective start date and time field, enter a date and time.</span></span>
7. <span data-ttu-id="2e82b-124">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="2e82b-124">Click Save.</span></span>

## <a name="create-a-carrier-fuel-index"></a><span data-ttu-id="2e82b-125">Opret et Brændstofindeks for fragt</span><span class="sxs-lookup"><span data-stu-id="2e82b-125">Create a Carrier fuel index</span></span>
1. <span data-ttu-id="2e82b-126">Gå til Transportstyring > Opsætning > Brændstofindekser > Brændstofindeks for fragt.</span><span class="sxs-lookup"><span data-stu-id="2e82b-126">Go to Transportation management > Setup > Fuel indexes > Carrier fuel indexes.</span></span>
2. <span data-ttu-id="2e82b-127">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="2e82b-127">Click New.</span></span>
3. <span data-ttu-id="2e82b-128">Indtast en værdi i feltet Brændstofindeks for fragt.</span><span class="sxs-lookup"><span data-stu-id="2e82b-128">In the Carrier fuel index field, type a value.</span></span>
4. <span data-ttu-id="2e82b-129">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="2e82b-129">In the Description field, type a value.</span></span>
5. <span data-ttu-id="2e82b-130">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="2e82b-130">Click New.</span></span>
6. <span data-ttu-id="2e82b-131">Angiv en dato og et klokkeslæt i feltet Gældende startdato og -klokkeslæt.</span><span class="sxs-lookup"><span data-stu-id="2e82b-131">In the Effective start date and time field, enter a date and time.</span></span>
7. <span data-ttu-id="2e82b-132">Angiv et tal i feltet PGG fra.</span><span class="sxs-lookup"><span data-stu-id="2e82b-132">In the PPG From field, enter a number.</span></span>
    * <span data-ttu-id="2e82b-133">I dette eksempel kan du angive feltet PPG fra til 1.95.</span><span class="sxs-lookup"><span data-stu-id="2e82b-133">In this example, you can set PPG From field to 1.95.</span></span>  
8. <span data-ttu-id="2e82b-134">Angiv et tal i feltet PGG til.</span><span class="sxs-lookup"><span data-stu-id="2e82b-134">In the PPG To field, enter a number.</span></span>
    * <span data-ttu-id="2e82b-135">I dette eksempel kan du angive feltet PPG til til 2.</span><span class="sxs-lookup"><span data-stu-id="2e82b-135">In this example you can set the PPG To field to 2.</span></span>  
9. <span data-ttu-id="2e82b-136">Angiv et tal i feltet Procent.</span><span class="sxs-lookup"><span data-stu-id="2e82b-136">In the Percentage field, enter a number.</span></span>
    * <span data-ttu-id="2e82b-137">I dette eksempel kan du angive procenten til 3.</span><span class="sxs-lookup"><span data-stu-id="2e82b-137">In this example you can set the percentage to 3.</span></span>  
10. <span data-ttu-id="2e82b-138">Klik på rullelisten i feltet Valuta for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="2e82b-138">In the Currency field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="2e82b-139">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="2e82b-139">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="2e82b-140">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="2e82b-140">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="2e82b-141">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="2e82b-141">Click Save.</span></span>


