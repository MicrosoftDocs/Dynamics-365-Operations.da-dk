---
title: Konfigurere et brændstofindeks for fragtmand
description: Denne vejledning viser, hvordan du opretter et område for brændstofindeks, et brændstofindeks og fragtmandens brændstofindeks.
author: ShylaThompson
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSFuelIndexRegion, TMSCarrierFuelIndexTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 33441de148b7edc8c564465d94ccf5602acbbe67
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016741"
---
# <a name="set-up-a-carrier-fuel-index"></a><span data-ttu-id="93cda-103">Konfigurere et brændstofindeks for fragtmand</span><span class="sxs-lookup"><span data-stu-id="93cda-103">Set up a carrier fuel index</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="93cda-104">Denne vejledning viser, hvordan du opretter et område for brændstofindeks, et brændstofindeks og fragtmandens brændstofindeks.</span><span class="sxs-lookup"><span data-stu-id="93cda-104">This guide shows how to create a fuel index region, a fuel index and a carrier fuel index.</span></span> <span data-ttu-id="93cda-105">Området for brændstofindeks angiver hvilket område brændstofindekset skal gælde for, og brændstofindekset angiver en brændstofpris for en bestemt tidsperiode.</span><span class="sxs-lookup"><span data-stu-id="93cda-105">The fuel index region specifies which region the fuel index should apply to, and the fuel index specifies a fuel price for a particular period of time.</span></span> <span data-ttu-id="93cda-106">For at afspejle ændringer i brændstofpriser over tid kan du knytte flere brændstofindekser til en fragtmand.</span><span class="sxs-lookup"><span data-stu-id="93cda-106">To reflect the change in fuel prices over time, you can associate multiple fuel indexes with a carrier.</span></span>  <span data-ttu-id="93cda-107">Disse opgaver udføres normalt af en transportkoordinator.</span><span class="sxs-lookup"><span data-stu-id="93cda-107">These tasks are normally done by a transportation coordinator.</span></span> <span data-ttu-id="93cda-108">Du kan bruge denne procedure i USMF-demodatafirmaet eller ved at bruge dine egne data.</span><span class="sxs-lookup"><span data-stu-id="93cda-108">You can use this procedure in demo data company USMF or using your own data.</span></span>


## <a name="create-a-fuel-index-region"></a><span data-ttu-id="93cda-109">Opret et område for brændstofindeks</span><span class="sxs-lookup"><span data-stu-id="93cda-109">Create a fuel index region</span></span>
1. <span data-ttu-id="93cda-110">Gå til Transportstyring > Opsætning > Brændstofindekser > Områder for brændstofindeks.</span><span class="sxs-lookup"><span data-stu-id="93cda-110">Go to Transportation management > Setup > Fuel indexes > Fuel index regions.</span></span>
    * <span data-ttu-id="93cda-111">Først er det nødvendigt at oprette forskellige områder, hvor du bruger og beregner forskellige brændstoftillæg.</span><span class="sxs-lookup"><span data-stu-id="93cda-111">First you have to create the different regions, where you operate and calculate different fuel surcharges.</span></span>  
2. <span data-ttu-id="93cda-112">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="93cda-112">Click New.</span></span>
3. <span data-ttu-id="93cda-113">Skriv en værdi i feltet Område.</span><span class="sxs-lookup"><span data-stu-id="93cda-113">In the Region field, type a value.</span></span>
4. <span data-ttu-id="93cda-114">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="93cda-114">In the Name field, type a value.</span></span>
5. <span data-ttu-id="93cda-115">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="93cda-115">Click Save.</span></span>

## <a name="create-a-fuel-index"></a><span data-ttu-id="93cda-116">Oprette et brændstofindeks</span><span class="sxs-lookup"><span data-stu-id="93cda-116">Create a fuel index</span></span>
1. <span data-ttu-id="93cda-117">Gå til Transportstyring > Opsætning > Brændstofindekser > Brændstofindekser.</span><span class="sxs-lookup"><span data-stu-id="93cda-117">Go to Transportation management > Setup > Fuel indexes > Fuel indexes.</span></span>
    * <span data-ttu-id="93cda-118">Du skal angive de aktuelle priser for brændstof for de områder, du har oprettet.</span><span class="sxs-lookup"><span data-stu-id="93cda-118">For the regions you have set up you need to enter the current prices for the fuel.</span></span>  
2. <span data-ttu-id="93cda-119">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="93cda-119">Click New.</span></span>
3. <span data-ttu-id="93cda-120">Klik på rullelisten i feltet Område for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="93cda-120">In the Region field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="93cda-121">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="93cda-121">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="93cda-122">Angiv et tal i feltet Pris pr. gallon.</span><span class="sxs-lookup"><span data-stu-id="93cda-122">In the Price per gallon field, enter a number.</span></span>
6. <span data-ttu-id="93cda-123">Angiv en dato og et klokkeslæt i feltet Gældende startdato og -klokkeslæt.</span><span class="sxs-lookup"><span data-stu-id="93cda-123">In the Effective start date and time field, enter a date and time.</span></span>
7. <span data-ttu-id="93cda-124">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="93cda-124">Click Save.</span></span>

## <a name="create-a-carrier-fuel-index"></a><span data-ttu-id="93cda-125">Opret et Brændstofindeks for fragt</span><span class="sxs-lookup"><span data-stu-id="93cda-125">Create a Carrier fuel index</span></span>
1. <span data-ttu-id="93cda-126">Gå til Transportstyring > Opsætning > Brændstofindekser > Brændstofindeks for fragt.</span><span class="sxs-lookup"><span data-stu-id="93cda-126">Go to Transportation management > Setup > Fuel indexes > Carrier fuel indexes.</span></span>
2. <span data-ttu-id="93cda-127">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="93cda-127">Click New.</span></span>
3. <span data-ttu-id="93cda-128">Indtast en værdi i feltet Brændstofindeks for fragt.</span><span class="sxs-lookup"><span data-stu-id="93cda-128">In the Carrier fuel index field, type a value.</span></span>
4. <span data-ttu-id="93cda-129">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="93cda-129">In the Description field, type a value.</span></span>
5. <span data-ttu-id="93cda-130">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="93cda-130">Click New.</span></span>
6. <span data-ttu-id="93cda-131">Angiv en dato og et klokkeslæt i feltet Gældende startdato og -klokkeslæt.</span><span class="sxs-lookup"><span data-stu-id="93cda-131">In the Effective start date and time field, enter a date and time.</span></span>
7. <span data-ttu-id="93cda-132">Angiv et tal i feltet PGG fra.</span><span class="sxs-lookup"><span data-stu-id="93cda-132">In the PPG From field, enter a number.</span></span>
    * <span data-ttu-id="93cda-133">I dette eksempel kan du angive feltet PPG fra til 1.95.</span><span class="sxs-lookup"><span data-stu-id="93cda-133">In this example, you can set PPG From field to 1.95.</span></span>  
8. <span data-ttu-id="93cda-134">Angiv et tal i feltet PGG til.</span><span class="sxs-lookup"><span data-stu-id="93cda-134">In the PPG To field, enter a number.</span></span>
    * <span data-ttu-id="93cda-135">I dette eksempel kan du angive feltet PPG til til 2.</span><span class="sxs-lookup"><span data-stu-id="93cda-135">In this example you can set the PPG To field to 2.</span></span>  
9. <span data-ttu-id="93cda-136">Angiv et tal i feltet Procent.</span><span class="sxs-lookup"><span data-stu-id="93cda-136">In the Percentage field, enter a number.</span></span>
    * <span data-ttu-id="93cda-137">I dette eksempel kan du angive procenten til 3.</span><span class="sxs-lookup"><span data-stu-id="93cda-137">In this example you can set the percentage to 3.</span></span>  
10. <span data-ttu-id="93cda-138">Klik på rullelisten i feltet Valuta for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="93cda-138">In the Currency field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="93cda-139">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="93cda-139">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="93cda-140">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="93cda-140">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="93cda-141">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="93cda-141">Click Save.</span></span>

