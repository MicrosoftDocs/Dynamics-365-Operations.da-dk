--- 
title: "Tilknytte et brændstofindeks med en fragtmand som tillægsgebyr"
description: "Denne vejledning viser, hvordan du opretter en tilbehørstildeling, tillægsgebyr for fragtmand, tillægsmaster for brændstoftillæg og knytter en fragtmands brændstofindeks til en fragtmand."
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: ae0aa90cfd673704bcd8e19f795499283ff01d44
ms.contentlocale: da-dk
ms.lasthandoff: 08/07/2018

---
# <a name="associate-a-fuel-index-with-a-carrier-as-an-accessorial-charge"></a><span data-ttu-id="2be8f-103">Tilknytte et brændstofindeks med en fragtmand som tillægsgebyr</span><span class="sxs-lookup"><span data-stu-id="2be8f-103">Associate a fuel index with a carrier as an accessorial charge</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2be8f-104">Denne vejledning viser, hvordan du opretter en tilbehørstildeling, tillægsgebyr for fragtmand, tillægsmaster for brændstoftillæg og knytter en fragtmands brændstofindeks til en fragtmand.</span><span class="sxs-lookup"><span data-stu-id="2be8f-104">This guide shows how to create an accessorial assignment, carrier accessorial charge, accessorial master for fuel surcharge, and associate a carrier fuel index with a carrier.</span></span> <span data-ttu-id="2be8f-105">Du skal have oprettet en fragtmands brændstofindeks, før du kører denne guide.</span><span class="sxs-lookup"><span data-stu-id="2be8f-105">You need to have set up a carrier fuel index before you run this guide.</span></span> <span data-ttu-id="2be8f-106">Du kan bruge guiden "Konfigurer brændstofindeks for en fragtmand" for at gøre dette.</span><span class="sxs-lookup"><span data-stu-id="2be8f-106">You can use the “Set up a carrier fuel index” guide to do this.</span></span> <span data-ttu-id="2be8f-107">Disse konfigurationsopgaver udføres typisk af en logistikchef.</span><span class="sxs-lookup"><span data-stu-id="2be8f-107">These setup tasks are typically done by a Logistics manager.</span></span> <span data-ttu-id="2be8f-108">De demodata, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="2be8f-108">The demo data used to create this procedure is USMF.</span></span>


## <a name="create-an-accessorial-master"></a><span data-ttu-id="2be8f-109">Opret en tillægsmaster</span><span class="sxs-lookup"><span data-stu-id="2be8f-109">Create an accessorial master</span></span>
1. <span data-ttu-id="2be8f-110">Gå til Transportstyring > Opsætning > Klassificering > Tilbehørsmastere.</span><span class="sxs-lookup"><span data-stu-id="2be8f-110">Go to Transportation management > Setup > Rating > Accessorial masters.</span></span>
2. <span data-ttu-id="2be8f-111">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="2be8f-111">Click New.</span></span>
3. <span data-ttu-id="2be8f-112">Skriv en værdi i feltet Tilbehørsmaster.</span><span class="sxs-lookup"><span data-stu-id="2be8f-112">In the Accessorial master field, type a value.</span></span>
4. <span data-ttu-id="2be8f-113">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="2be8f-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="2be8f-114">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="2be8f-114">Click Save.</span></span>

## <a name="create-a-carrier-accessorial-charge"></a><span data-ttu-id="2be8f-115">Opret et tillægsgebyr for fragtmand</span><span class="sxs-lookup"><span data-stu-id="2be8f-115">Create a carrier accessorial charge</span></span>
1. <span data-ttu-id="2be8f-116">Gå til Transportstyring > Opsætning > Klassificering > Fragtmands tillægsgebyrer.</span><span class="sxs-lookup"><span data-stu-id="2be8f-116">Go to Transportation management > Setup > Rating > Carrier accessorial charges.</span></span>
2. <span data-ttu-id="2be8f-117">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="2be8f-117">Click New.</span></span>
3. <span data-ttu-id="2be8f-118">Indtast en værdi i feltet Id for fragtmandstilbehør.</span><span class="sxs-lookup"><span data-stu-id="2be8f-118">In the Carrier accessorial ID field, type a value.</span></span>
4. <span data-ttu-id="2be8f-119">Klik på rullelisten i feltet Fragtmand for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="2be8f-119">In the Shipping carrier field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="2be8f-120">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="2be8f-120">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="2be8f-121">I dette eksempel skal du vælge lastbilsfragtmand.</span><span class="sxs-lookup"><span data-stu-id="2be8f-121">In this example, choose Truck Carrier.</span></span>  
6. <span data-ttu-id="2be8f-122">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="2be8f-122">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="2be8f-123">Klik på rullelisten i feltet Fragttjeneste for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="2be8f-123">In the Carrier service field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="2be8f-124">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="2be8f-124">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="2be8f-125">Klik på rullelisten i feltet Tilbehørsmaster for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="2be8f-125">In the Accessorial master field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="2be8f-126">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="2be8f-126">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="2be8f-127">I dette eksempel skal du vælge den nyoprettede Tilbehørsmaster.</span><span class="sxs-lookup"><span data-stu-id="2be8f-127">In this example, choose the newly created Accessorial master.</span></span>  
11. <span data-ttu-id="2be8f-128">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="2be8f-128">Click Save.</span></span>

## <a name="create-an-accessorial-assignment"></a><span data-ttu-id="2be8f-129">Opret en tilbehørstildeling</span><span class="sxs-lookup"><span data-stu-id="2be8f-129">Create an accessorial assignment</span></span>
1. <span data-ttu-id="2be8f-130">Klik Tildelinger af tillæg.</span><span class="sxs-lookup"><span data-stu-id="2be8f-130">Click Accessorial assignments.</span></span>
2. <span data-ttu-id="2be8f-131">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="2be8f-131">Click New.</span></span>
3. <span data-ttu-id="2be8f-132">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="2be8f-132">In the Name field, type a value.</span></span>
4. <span data-ttu-id="2be8f-133">Slå udvidelsen af Sektionen Kriterier til/fra.</span><span class="sxs-lookup"><span data-stu-id="2be8f-133">Toggle the expansion of the Criteria section.</span></span>
    * <span data-ttu-id="2be8f-134">I kriterierne kan du vælge altid at anvende brændstoftillægget, eller for dette eksempel vælge, at det kun gælder inden for en bestemt region.</span><span class="sxs-lookup"><span data-stu-id="2be8f-134">In the criteria, you can choose to always apply the fuel surcharge or for this example choose that it only applies within a certain region.</span></span>  
5. <span data-ttu-id="2be8f-135">Skriv en værdi i feltet Postnummer fra.</span><span class="sxs-lookup"><span data-stu-id="2be8f-135">In the ZIP/postal code from field, type a value.</span></span>
6. <span data-ttu-id="2be8f-136">Skriv en værdi i feltet Postnummer til.</span><span class="sxs-lookup"><span data-stu-id="2be8f-136">In the ZIP/postal code to field, type a value.</span></span>
7. <span data-ttu-id="2be8f-137">Slå udvidelsen af sektionen Beregning til/fra.</span><span class="sxs-lookup"><span data-stu-id="2be8f-137">Toggle the expansion of the Calculation section.</span></span>
    * <span data-ttu-id="2be8f-138">I beregningssektionen kan du angive, hvordan brændstoftillægget beregnes.</span><span class="sxs-lookup"><span data-stu-id="2be8f-138">In the calculation section you can specify how to calculate the fuel surcharge.</span></span> <span data-ttu-id="2be8f-139">Denne beregning afhænger af den Tillægsenhed, som du har valgt som basis for beregningen.</span><span class="sxs-lookup"><span data-stu-id="2be8f-139">This calculation depends on the Accessorial unit that you chose as the base for your calculation.</span></span>  
8. <span data-ttu-id="2be8f-140">Vælg "Brændstoftillæg" i feltet Gebyrtype for tillæg.</span><span class="sxs-lookup"><span data-stu-id="2be8f-140">In the Accessorial fee type field, select 'Fuel surcharge'.</span></span>
9. <span data-ttu-id="2be8f-141">Vælg en "Kilometertal" i feltet Tillægsenhed.</span><span class="sxs-lookup"><span data-stu-id="2be8f-141">In the Accessorial unit field, select 'Mileage'.</span></span>
10. <span data-ttu-id="2be8f-142">Klik på rullelisten i feltet Område for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="2be8f-142">In the Region field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="2be8f-143">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="2be8f-143">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="2be8f-144">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="2be8f-144">Click Save.</span></span>

## <a name="update-the-carrier-rating-profile"></a><span data-ttu-id="2be8f-145">Opdater fragtmandens vurderingsprofil</span><span class="sxs-lookup"><span data-stu-id="2be8f-145">Update the carrier rating profile</span></span>
1. <span data-ttu-id="2be8f-146">Gå til Transportstyring > Opsætning > Fragtmænd > Fragtmænd.</span><span class="sxs-lookup"><span data-stu-id="2be8f-146">Go to Transportation management > Setup > Carriers > Shipping carriers.</span></span>
2. <span data-ttu-id="2be8f-147">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="2be8f-147">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="2be8f-148">Slå udvidelsen af sektionen Vurderingsprofiler til/fra.</span><span class="sxs-lookup"><span data-stu-id="2be8f-148">Toggle the expansion of the Rating profiles section.</span></span>
4. <span data-ttu-id="2be8f-149">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="2be8f-149">Click Edit.</span></span>
5. <span data-ttu-id="2be8f-150">Klik på rullelisten i feltet Brændstofindeks for fragt for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="2be8f-150">In the Carrier fuel index field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="2be8f-151">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="2be8f-151">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="2be8f-152">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="2be8f-152">Click Save.</span></span>


