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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 81f3244ff42cf13cd93ac10656c47f8a9204ef99
ms.contentlocale: da-dk
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-a-carrier-fuel-index"></a><span data-ttu-id="0a165-103">Konfigurere et brændstofindeks for fragtmand</span><span class="sxs-lookup"><span data-stu-id="0a165-103">Set up a carrier fuel index</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0a165-104">Denne vejledning viser, hvordan du opretter et område for brændstofindeks, et brændstofindeks og fragtmandens brændstofindeks.</span><span class="sxs-lookup"><span data-stu-id="0a165-104">This guide shows how to create a fuel index region, a fuel index and a carrier fuel index.</span></span> <span data-ttu-id="0a165-105">Området for brændstofindeks angiver hvilket område brændstofindekset skal gælde for, og brændstofindekset angiver en brændstofpris for en bestemt tidsperiode.</span><span class="sxs-lookup"><span data-stu-id="0a165-105">The fuel index region specifies which region the fuel index should apply to, and the fuel index specifies a fuel price for a particular period of time.</span></span> <span data-ttu-id="0a165-106">For at afspejle ændringer i brændstofpriser over tid kan du knytte flere brændstofindekser til en fragtmand.</span><span class="sxs-lookup"><span data-stu-id="0a165-106">To reflect the change in fuel prices over time, you can associate multiple fuel indexes with a carrier.</span></span>  <span data-ttu-id="0a165-107">Disse opgaver udføres normalt af en transportkoordinator.</span><span class="sxs-lookup"><span data-stu-id="0a165-107">These tasks are normally done by a transportation coordinator.</span></span> <span data-ttu-id="0a165-108">Du kan bruge denne procedure i USMF-demodatafirmaet eller ved at bruge dine egne data.</span><span class="sxs-lookup"><span data-stu-id="0a165-108">You can use this procedure in demo data company USMF or using your own data.</span></span>


## <a name="create-a-fuel-index-region"></a><span data-ttu-id="0a165-109">Opret et område for brændstofindeks</span><span class="sxs-lookup"><span data-stu-id="0a165-109">Create a fuel index region</span></span>
1. <span data-ttu-id="0a165-110">Gå til Transportstyring > Opsætning > Brændstofindekser > Områder for brændstofindeks.</span><span class="sxs-lookup"><span data-stu-id="0a165-110">Go to Transportation management > Setup > Fuel indexes > Fuel index regions.</span></span>
    * <span data-ttu-id="0a165-111">Først er det nødvendigt at oprette forskellige områder, hvor du bruger og beregner forskellige brændstoftillæg.</span><span class="sxs-lookup"><span data-stu-id="0a165-111">First you have to create the different regions, where you operate and calculate different fuel surcharges.</span></span>  
2. <span data-ttu-id="0a165-112">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="0a165-112">Click New.</span></span>
3. <span data-ttu-id="0a165-113">Skriv en værdi i feltet Område.</span><span class="sxs-lookup"><span data-stu-id="0a165-113">In the Region field, type a value.</span></span>
4. <span data-ttu-id="0a165-114">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="0a165-114">In the Name field, type a value.</span></span>
5. <span data-ttu-id="0a165-115">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="0a165-115">Click Save.</span></span>

## <a name="create-a-fuel-index"></a><span data-ttu-id="0a165-116">Oprette et brændstofindeks</span><span class="sxs-lookup"><span data-stu-id="0a165-116">Create a fuel index</span></span>
1. <span data-ttu-id="0a165-117">Gå til Transportstyring > Opsætning > Brændstofindekser > Brændstofindekser.</span><span class="sxs-lookup"><span data-stu-id="0a165-117">Go to Transportation management > Setup > Fuel indexes > Fuel indexes.</span></span>
    * <span data-ttu-id="0a165-118">Du skal angive de aktuelle priser for brændstof for de områder, du har oprettet.</span><span class="sxs-lookup"><span data-stu-id="0a165-118">For the regions you have set up you need to enter the current prices for the fuel.</span></span>  
2. <span data-ttu-id="0a165-119">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="0a165-119">Click New.</span></span>
3. <span data-ttu-id="0a165-120">Klik på rullelisten i feltet Område for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="0a165-120">In the Region field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="0a165-121">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="0a165-121">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="0a165-122">Angiv et tal i feltet Pris pr. gallon.</span><span class="sxs-lookup"><span data-stu-id="0a165-122">In the Price per gallon field, enter a number.</span></span>
6. <span data-ttu-id="0a165-123">Angiv en dato og et klokkeslæt i feltet Gældende startdato og -klokkeslæt.</span><span class="sxs-lookup"><span data-stu-id="0a165-123">In the Effective start date and time field, enter a date and time.</span></span>
7. <span data-ttu-id="0a165-124">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="0a165-124">Click Save.</span></span>

## <a name="create-a-carrier-fuel-index"></a><span data-ttu-id="0a165-125">Opret et Brændstofindeks for fragt</span><span class="sxs-lookup"><span data-stu-id="0a165-125">Create a Carrier fuel index</span></span>
1. <span data-ttu-id="0a165-126">Gå til Transportstyring > Opsætning > Brændstofindekser > Brændstofindeks for fragt.</span><span class="sxs-lookup"><span data-stu-id="0a165-126">Go to Transportation management > Setup > Fuel indexes > Carrier fuel indexes.</span></span>
2. <span data-ttu-id="0a165-127">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="0a165-127">Click New.</span></span>
3. <span data-ttu-id="0a165-128">Indtast en værdi i feltet Brændstofindeks for fragt.</span><span class="sxs-lookup"><span data-stu-id="0a165-128">In the Carrier fuel index field, type a value.</span></span>
4. <span data-ttu-id="0a165-129">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="0a165-129">In the Description field, type a value.</span></span>
5. <span data-ttu-id="0a165-130">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="0a165-130">Click New.</span></span>
6. <span data-ttu-id="0a165-131">Angiv en dato og et klokkeslæt i feltet Gældende startdato og -klokkeslæt.</span><span class="sxs-lookup"><span data-stu-id="0a165-131">In the Effective start date and time field, enter a date and time.</span></span>
7. <span data-ttu-id="0a165-132">Angiv et tal i feltet PGG fra.</span><span class="sxs-lookup"><span data-stu-id="0a165-132">In the PPG From field, enter a number.</span></span>
    * <span data-ttu-id="0a165-133">I dette eksempel kan du angive feltet PPG fra til 1.95.</span><span class="sxs-lookup"><span data-stu-id="0a165-133">In this example, you can set PPG From field to 1.95.</span></span>  
8. <span data-ttu-id="0a165-134">Angiv et tal i feltet PGG til.</span><span class="sxs-lookup"><span data-stu-id="0a165-134">In the PPG To field, enter a number.</span></span>
    * <span data-ttu-id="0a165-135">I dette eksempel kan du angive feltet PPG til til 2.</span><span class="sxs-lookup"><span data-stu-id="0a165-135">In this example you can set the PPG To field to 2.</span></span>  
9. <span data-ttu-id="0a165-136">Angiv et tal i feltet Procent.</span><span class="sxs-lookup"><span data-stu-id="0a165-136">In the Percentage field, enter a number.</span></span>
    * <span data-ttu-id="0a165-137">I dette eksempel kan du angive procenten til 3.</span><span class="sxs-lookup"><span data-stu-id="0a165-137">In this example you can set the percentage to 3.</span></span>  
10. <span data-ttu-id="0a165-138">Klik på rullelisten i feltet Valuta for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="0a165-138">In the Currency field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="0a165-139">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="0a165-139">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="0a165-140">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="0a165-140">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="0a165-141">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="0a165-141">Click Save.</span></span>


