---
title: Tilknytte et brændstofindeks med en fragtmand som tillægsgebyr
description: Denne vejledning viser, hvordan du opretter en tilbehørstildeling, tillægsgebyr for fragtmand, tillægsmaster for brændstoftillæg og knytter en fragtmands brændstofindeks til en fragtmand.
author: ShylaThompson
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSRatingProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a1f69a6350a5a84ed19dcb37e174c25b112c16bd
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974129"
---
# <a name="associate-a-fuel-index-with-a-carrier-as-an-accessorial-charge"></a><span data-ttu-id="755b9-103">Tilknytte et brændstofindeks med en fragtmand som tillægsgebyr</span><span class="sxs-lookup"><span data-stu-id="755b9-103">Associate a fuel index with a carrier as an accessorial charge</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="755b9-104">Denne vejledning viser, hvordan du opretter en tilbehørstildeling, tillægsgebyr for fragtmand, tillægsmaster for brændstoftillæg og knytter en fragtmands brændstofindeks til en fragtmand.</span><span class="sxs-lookup"><span data-stu-id="755b9-104">This guide shows how to create an accessorial assignment, carrier accessorial charge, accessorial master for fuel surcharge, and associate a carrier fuel index with a carrier.</span></span> <span data-ttu-id="755b9-105">Du skal have oprettet en fragtmands brændstofindeks, før du kører denne guide.</span><span class="sxs-lookup"><span data-stu-id="755b9-105">You need to have set up a carrier fuel index before you run this guide.</span></span> <span data-ttu-id="755b9-106">Du kan bruge guiden "Konfigurer brændstofindeks for en fragtmand" for at gøre dette.</span><span class="sxs-lookup"><span data-stu-id="755b9-106">You can use the "Set up a carrier fuel index" guide to do this.</span></span> <span data-ttu-id="755b9-107">Disse konfigurationsopgaver udføres typisk af en logistikchef.</span><span class="sxs-lookup"><span data-stu-id="755b9-107">These setup tasks are typically done by a Logistics manager.</span></span> <span data-ttu-id="755b9-108">De demodata, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="755b9-108">The demo data used to create this procedure is USMF.</span></span>


## <a name="create-an-accessorial-master"></a><span data-ttu-id="755b9-109">Opret en tillægsmaster</span><span class="sxs-lookup"><span data-stu-id="755b9-109">Create an accessorial master</span></span>
1. <span data-ttu-id="755b9-110">Gå til Transportstyring > Opsætning > Klassificering > Tilbehørsmastere.</span><span class="sxs-lookup"><span data-stu-id="755b9-110">Go to Transportation management > Setup > Rating > Accessorial masters.</span></span>
2. <span data-ttu-id="755b9-111">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="755b9-111">Click New.</span></span>
3. <span data-ttu-id="755b9-112">Skriv en værdi i feltet Tilbehørsmaster.</span><span class="sxs-lookup"><span data-stu-id="755b9-112">In the Accessorial master field, type a value.</span></span>
4. <span data-ttu-id="755b9-113">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="755b9-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="755b9-114">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="755b9-114">Click Save.</span></span>

## <a name="create-a-carrier-accessorial-charge"></a><span data-ttu-id="755b9-115">Opret et tillægsgebyr for fragtmand</span><span class="sxs-lookup"><span data-stu-id="755b9-115">Create a carrier accessorial charge</span></span>
1. <span data-ttu-id="755b9-116">Gå til Transportstyring > Opsætning > Klassificering > Fragtmands tillægsgebyrer.</span><span class="sxs-lookup"><span data-stu-id="755b9-116">Go to Transportation management > Setup > Rating > Carrier accessorial charges.</span></span>
2. <span data-ttu-id="755b9-117">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="755b9-117">Click New.</span></span>
3. <span data-ttu-id="755b9-118">Indtast en værdi i feltet Id for fragtmandstilbehør.</span><span class="sxs-lookup"><span data-stu-id="755b9-118">In the Carrier accessorial ID field, type a value.</span></span>
4. <span data-ttu-id="755b9-119">Klik på rullelisten i feltet Fragtmand for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="755b9-119">In the Shipping carrier field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="755b9-120">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="755b9-120">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="755b9-121">I dette eksempel skal du vælge lastbilsfragtmand.</span><span class="sxs-lookup"><span data-stu-id="755b9-121">In this example, choose Truck Carrier.</span></span>  
6. <span data-ttu-id="755b9-122">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="755b9-122">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="755b9-123">Klik på rullelisten i feltet Fragttjeneste for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="755b9-123">In the Carrier service field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="755b9-124">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="755b9-124">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="755b9-125">Klik på rullelisten i feltet Tilbehørsmaster for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="755b9-125">In the Accessorial master field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="755b9-126">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="755b9-126">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="755b9-127">I dette eksempel skal du vælge den nyoprettede Tilbehørsmaster.</span><span class="sxs-lookup"><span data-stu-id="755b9-127">In this example, choose the newly created Accessorial master.</span></span>  
11. <span data-ttu-id="755b9-128">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="755b9-128">Click Save.</span></span>

## <a name="create-an-accessorial-assignment"></a><span data-ttu-id="755b9-129">Opret en tilbehørstildeling</span><span class="sxs-lookup"><span data-stu-id="755b9-129">Create an accessorial assignment</span></span>
1. <span data-ttu-id="755b9-130">Klik Tildelinger af tillæg.</span><span class="sxs-lookup"><span data-stu-id="755b9-130">Click Accessorial assignments.</span></span>
2. <span data-ttu-id="755b9-131">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="755b9-131">Click New.</span></span>
3. <span data-ttu-id="755b9-132">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="755b9-132">In the Name field, type a value.</span></span>
4. <span data-ttu-id="755b9-133">Slå udvidelsen af Sektionen Kriterier til/fra.</span><span class="sxs-lookup"><span data-stu-id="755b9-133">Toggle the expansion of the Criteria section.</span></span>
    * <span data-ttu-id="755b9-134">I kriterierne kan du vælge altid at anvende brændstoftillægget, eller for dette eksempel vælge, at det kun gælder inden for en bestemt region.</span><span class="sxs-lookup"><span data-stu-id="755b9-134">In the criteria, you can choose to always apply the fuel surcharge or for this example choose that it only applies within a certain region.</span></span>  
5. <span data-ttu-id="755b9-135">Skriv en værdi i feltet Postnummer fra.</span><span class="sxs-lookup"><span data-stu-id="755b9-135">In the ZIP/postal code from field, type a value.</span></span>
6. <span data-ttu-id="755b9-136">Skriv en værdi i feltet Postnummer til.</span><span class="sxs-lookup"><span data-stu-id="755b9-136">In the ZIP/postal code to field, type a value.</span></span>
7. <span data-ttu-id="755b9-137">Slå udvidelsen af sektionen Beregning til/fra.</span><span class="sxs-lookup"><span data-stu-id="755b9-137">Toggle the expansion of the Calculation section.</span></span>
    * <span data-ttu-id="755b9-138">I beregningssektionen kan du angive, hvordan brændstoftillægget beregnes.</span><span class="sxs-lookup"><span data-stu-id="755b9-138">In the calculation section you can specify how to calculate the fuel surcharge.</span></span> <span data-ttu-id="755b9-139">Denne beregning afhænger af den Tillægsenhed, som du har valgt som basis for beregningen.</span><span class="sxs-lookup"><span data-stu-id="755b9-139">This calculation depends on the Accessorial unit that you chose as the base for your calculation.</span></span>  
8. <span data-ttu-id="755b9-140">Vælg "Brændstoftillæg" i feltet Gebyrtype for tillæg.</span><span class="sxs-lookup"><span data-stu-id="755b9-140">In the Accessorial fee type field, select 'Fuel surcharge'.</span></span>
9. <span data-ttu-id="755b9-141">Vælg en "Kilometertal" i feltet Tillægsenhed.</span><span class="sxs-lookup"><span data-stu-id="755b9-141">In the Accessorial unit field, select 'Mileage'.</span></span>
10. <span data-ttu-id="755b9-142">Klik på rullelisten i feltet Område for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="755b9-142">In the Region field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="755b9-143">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="755b9-143">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="755b9-144">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="755b9-144">Click Save.</span></span>

## <a name="update-the-carrier-rating-profile"></a><span data-ttu-id="755b9-145">Opdater fragtmandens vurderingsprofil</span><span class="sxs-lookup"><span data-stu-id="755b9-145">Update the carrier rating profile</span></span>
1. <span data-ttu-id="755b9-146">Gå til Transportstyring > Opsætning > Fragtmænd > Fragtmænd.</span><span class="sxs-lookup"><span data-stu-id="755b9-146">Go to Transportation management > Setup > Carriers > Shipping carriers.</span></span>
2. <span data-ttu-id="755b9-147">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="755b9-147">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="755b9-148">Slå udvidelsen af sektionen Vurderingsprofiler til/fra.</span><span class="sxs-lookup"><span data-stu-id="755b9-148">Toggle the expansion of the Rating profiles section.</span></span>
4. <span data-ttu-id="755b9-149">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="755b9-149">Click Edit.</span></span>
5. <span data-ttu-id="755b9-150">Klik på rullelisten i feltet Brændstofindeks for fragt for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="755b9-150">In the Carrier fuel index field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="755b9-151">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="755b9-151">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="755b9-152">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="755b9-152">Click Save.</span></span>

