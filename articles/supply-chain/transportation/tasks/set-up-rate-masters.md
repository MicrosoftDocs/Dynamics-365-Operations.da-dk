--- 
title: Konfigurere satsmastere
description: Denne procedure viser, hvordan du opretter en satsmaster.
author: BibiSp
manager: AnnBe
ms.date: 11/11/2016
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
ms.openlocfilehash: a3ba01bc05d130991e8a744d9026d53edf93ee20
ms.contentlocale: da-dk
ms.lasthandoff: 04/13/2018

---
# <a name="set-up-rate-masters"></a><span data-ttu-id="35ced-103">Konfigurere satsmastere</span><span class="sxs-lookup"><span data-stu-id="35ced-103">Set up rate masters</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="35ced-104">Denne procedure viser, hvordan du opretter en satsmaster.</span><span class="sxs-lookup"><span data-stu-id="35ced-104">This procedure shows you how to set up a rate master.</span></span> <span data-ttu-id="35ced-105">Logistikchefen konfigurerer normalt satsmastere, afhængigt af kontrakterne der er signeret med fragtmændene.</span><span class="sxs-lookup"><span data-stu-id="35ced-105">The logistic manager usually sets up rate masters, depending on the contracts signed with the carriers.</span></span> <span data-ttu-id="35ced-106">I dette scenario skal du konfigurer en satsmaster for en fragtmand.</span><span class="sxs-lookup"><span data-stu-id="35ced-106">In this scenario you will set up a rate master for an air carrier.</span></span> <span data-ttu-id="35ced-107">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="35ced-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-rate-master"></a><span data-ttu-id="35ced-108">Konfigurer satsmaster</span><span class="sxs-lookup"><span data-stu-id="35ced-108">Set up rate master</span></span>
1. <span data-ttu-id="35ced-109">Gå til Transportstyring > Opsætning > Klassificering > Satsmaster.</span><span class="sxs-lookup"><span data-stu-id="35ced-109">Go to Transportation management > Setup > Rating > Rate master.</span></span>
2. <span data-ttu-id="35ced-110">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="35ced-110">Click New.</span></span>
3. <span data-ttu-id="35ced-111">Skriv en værdi i feltet Satsmaster.</span><span class="sxs-lookup"><span data-stu-id="35ced-111">In the Rate master field, type a value.</span></span>
4. <span data-ttu-id="35ced-112">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="35ced-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="35ced-113">Klik på rullelisten i feltet Vurderingsmetadata-id for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="35ced-113">In the Rating metadata ID field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="35ced-114">Vurderingsmetadata-id'et bestemmer de data, der er nødvendige for satsmasteren, da det definerer de metadata, der forventes af TMS-programmet, der bruger denne satsmaster.</span><span class="sxs-lookup"><span data-stu-id="35ced-114">The rating metadata ID will determine the data needed for the rate master, as it defines the metadata expected by the TMS engine using this rate master.</span></span>  
6. <span data-ttu-id="35ced-115">Vælg P2P-indstillingen til dette eksempel</span><span class="sxs-lookup"><span data-stu-id="35ced-115">For this example, select the P2P option</span></span>
7. <span data-ttu-id="35ced-116">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="35ced-116">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="35ced-117">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="35ced-117">Click Save.</span></span>

## <a name="set-up-rate-base"></a><span data-ttu-id="35ced-118">Konfigurer satsgrundlag</span><span class="sxs-lookup"><span data-stu-id="35ced-118">Set up rate base</span></span>
1. <span data-ttu-id="35ced-119">Klik på Satsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="35ced-119">Click Rate base.</span></span>
    * <span data-ttu-id="35ced-120">Satsgrundlaget bestemmer satsen for fragtmanden og kan bruges til at konfigurere en tarifstruktur, da den strukturerer satserne i pausepunkterne, der er defineret i pausemasteren.</span><span class="sxs-lookup"><span data-stu-id="35ced-120">The rate base determines the rate of the carrier, and can be used to set up a tariff structure as it structures the rates in the breakpoints defined in the break master.</span></span>  
2. <span data-ttu-id="35ced-121">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="35ced-121">Click New.</span></span>
3. <span data-ttu-id="35ced-122">Skriv en værdi i feltet Satsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="35ced-122">In the Rate base field, type a value.</span></span>
4. <span data-ttu-id="35ced-123">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="35ced-123">In the Name field, type a value.</span></span>
5. <span data-ttu-id="35ced-124">Klik på rullelisten i feltet Pausemaster for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="35ced-124">In the Break master field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="35ced-125">Pausemastere bruges til at definere prisstrukturen og dens pausepunkter.</span><span class="sxs-lookup"><span data-stu-id="35ced-125">Break masters are used to define the pricing structure and its breakpoints.</span></span> <span data-ttu-id="35ced-126">Prisstrukturen bruger lagdelte priser, der er baseret på fysiske dimensioner.</span><span class="sxs-lookup"><span data-stu-id="35ced-126">The pricing structure uses tiered pricing that is based on physical dimensions.</span></span>  
6. <span data-ttu-id="35ced-127">I dette eksempel skal du bruge vægt</span><span class="sxs-lookup"><span data-stu-id="35ced-127">For this example, use weight</span></span>
7. <span data-ttu-id="35ced-128">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="35ced-128">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="35ced-129">Slå udvidelsen af sektionen afsnittet Detaljer til/fra.</span><span class="sxs-lookup"><span data-stu-id="35ced-129">Toggle the expansion of the Details section.</span></span>
9. <span data-ttu-id="35ced-130">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="35ced-130">Click New.</span></span>
10. <span data-ttu-id="35ced-131">Skriv "30301" i feltet Postnummer på levering andet sted.</span><span class="sxs-lookup"><span data-stu-id="35ced-131">In the Drop-off Postal Code From field, type '30301'.</span></span>
11. <span data-ttu-id="35ced-132">Skriv "30318" i feltet Til postnummer på levering andet sted.</span><span class="sxs-lookup"><span data-stu-id="35ced-132">In the Drop-off Postal Code To field, type '30318'.</span></span>
12. <span data-ttu-id="35ced-133">Skriv "USA" i feltet Land/område for levering andet sted.</span><span class="sxs-lookup"><span data-stu-id="35ced-133">In the Drop-off Country Region field, type 'USA'.</span></span>
13. <span data-ttu-id="35ced-134">Skriv "100" i feltet <1.00 Lbs.</span><span class="sxs-lookup"><span data-stu-id="35ced-134">In the <1.00 Lbs field, type '100'.</span></span>
    * <span data-ttu-id="35ced-135">Indsæt satsen pr. lbs, hvis den samlede vægt af belastningen er mindre end 1 pund.</span><span class="sxs-lookup"><span data-stu-id="35ced-135">Insert the rate per lbs if the total weight of the load is less than 1 pound.</span></span>  
14. <span data-ttu-id="35ced-136">Skriv "300" i feltet <5.00 Lbs.</span><span class="sxs-lookup"><span data-stu-id="35ced-136">In the <5.00 Lbs field, type '300'.</span></span>
    * <span data-ttu-id="35ced-137">Indsæt satsen pr. lbs, hvis den samlede vægt af belastningen er mindre end 5 pund.</span><span class="sxs-lookup"><span data-stu-id="35ced-137">Insert the rate per lbs if the total weight of the load is less than 5 pounds.</span></span>  
15. <span data-ttu-id="35ced-138">Skriv "500" i feltet <20.00 Lbs.</span><span class="sxs-lookup"><span data-stu-id="35ced-138">In the <20.00 Lbs field, type '500'.</span></span>
    * <span data-ttu-id="35ced-139">Indsæt satsen pr. lbs, hvis den samlede vægt af belastningen er mindre end 20 pund.</span><span class="sxs-lookup"><span data-stu-id="35ced-139">Insert the rate per lbs if the total weight of the load is less than 20 pounds.</span></span>  
16. <span data-ttu-id="35ced-140">Skriv "1000" i feltet <100.00 Lbs.</span><span class="sxs-lookup"><span data-stu-id="35ced-140">In the <100.00 Lbs field, type '1000'.</span></span>
    * <span data-ttu-id="35ced-141">Indsæt satsen pr. lbs, hvis den samlede vægt af belastningen er mindre end 100 pund.</span><span class="sxs-lookup"><span data-stu-id="35ced-141">Insert the rate per lbs if the total weight of the load is less than 100 pounds.</span></span>  
17. <span data-ttu-id="35ced-142">Skriv "3000" i feltet <1,000.00 Lbs.</span><span class="sxs-lookup"><span data-stu-id="35ced-142">In the <1,000.00 Lbs field, type '3000'.</span></span>
    * <span data-ttu-id="35ced-143">Indsæt satsen pr. lbs, hvis den samlede vægt af belastningen er mindre end 1000 pund.</span><span class="sxs-lookup"><span data-stu-id="35ced-143">Insert the rate per lbs if the total weight of the load is less than 1000 pounds.</span></span>  
18. <span data-ttu-id="35ced-144">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="35ced-144">Click Save.</span></span>
19. <span data-ttu-id="35ced-145">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="35ced-145">Close the page.</span></span>

## <a name="assign-rate-base"></a><span data-ttu-id="35ced-146">Tildel satsgrundlag</span><span class="sxs-lookup"><span data-stu-id="35ced-146">Assign rate base</span></span>
1. <span data-ttu-id="35ced-147">Slå udvidelsen af sektionen Tildelinger af satsgrundlag til/fra.</span><span class="sxs-lookup"><span data-stu-id="35ced-147">Toggle the expansion of the Rate base assignments section.</span></span>
2. <span data-ttu-id="35ced-148">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="35ced-148">Click New.</span></span>
    * <span data-ttu-id="35ced-149">Du kan have flere tildelinger af satsgrundlag for hver satsmaster.</span><span class="sxs-lookup"><span data-stu-id="35ced-149">You can have several rate base assignments for each rate master.</span></span> <span data-ttu-id="35ced-150">Det gør det muligt at oprette flere forskellige prispointer for hver fragtmand afhængigt af destinationer, tjenester eller andre satsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="35ced-150">This makes it possible to create several different price points for each carrier depending on destinations, services, or different rate bases.</span></span> <span data-ttu-id="35ced-151">I denne procedure skal du kun oprette én satsbasistildeling.</span><span class="sxs-lookup"><span data-stu-id="35ced-151">In this procedure you will only create one rate base assignment.</span></span>  
3. <span data-ttu-id="35ced-152">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="35ced-152">In the Name field, type a value.</span></span>
4. <span data-ttu-id="35ced-153">Klik på rullelisten i feltet Satsgrundlag for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="35ced-153">In the Rate base field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="35ced-154">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="35ced-154">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="35ced-155">Klik på rullelisten i feltet Ydelse for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="35ced-155">In the Service field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="35ced-156">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="35ced-156">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="35ced-157">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="35ced-157">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="35ced-158">Skriv "98052" i feltet Postnummer på afhentning.</span><span class="sxs-lookup"><span data-stu-id="35ced-158">In the Pick-up Postal Code field, type '98052'.</span></span>
    * <span data-ttu-id="35ced-159">Angiv, hvilket postnummer denne satsbasistildeling skal være gyldig fra.</span><span class="sxs-lookup"><span data-stu-id="35ced-159">Specify which postal code this rate base assignment should be valid from.</span></span>    
10. <span data-ttu-id="35ced-160">Skriv "USA" i feltet Afhentningsland/område.</span><span class="sxs-lookup"><span data-stu-id="35ced-160">In the Pick-up Country Region field, type 'USA'.</span></span>
11. <span data-ttu-id="35ced-161">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="35ced-161">Click Save.</span></span>


