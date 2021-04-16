---
title: Konfigurere satsmastere
description: Denne procedure viser, hvordan du opretter en satsmaster.
author: ShylaThompson
ms.date: 10/16/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSBreakMaster,TMSRateMaster,TMSRateMasterBase,TMSRateBaseType, TMSRouteWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8cb25726e05f11420c7355c39f7e262abca5da62
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808984"
---
# <a name="set-up-rate-masters"></a><span data-ttu-id="49fbf-103">Konfigurere satsmastere</span><span class="sxs-lookup"><span data-stu-id="49fbf-103">Set up rate masters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="49fbf-104">Denne procedure viser, hvordan du opretter en satsmaster.</span><span class="sxs-lookup"><span data-stu-id="49fbf-104">This procedure shows you how to set up a rate master.</span></span> <span data-ttu-id="49fbf-105">Logistikchefen konfigurerer normalt satsmastere, afhængigt af kontrakterne der er signeret med fragtmændene.</span><span class="sxs-lookup"><span data-stu-id="49fbf-105">The logistic manager usually sets up rate masters, depending on the contracts signed with the carriers.</span></span> <span data-ttu-id="49fbf-106">I dette scenario skal du konfigurer en satsmaster for en fragtmand.</span><span class="sxs-lookup"><span data-stu-id="49fbf-106">In this scenario you will set up a rate master for an air carrier.</span></span> <span data-ttu-id="49fbf-107">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="49fbf-107">The demo data company used to create this procedure is USMF.</span></span>

## <a name="set-up-break-master"></a><span data-ttu-id="49fbf-108">Konfigurere en pausemaster</span><span class="sxs-lookup"><span data-stu-id="49fbf-108">Set up break master</span></span>

1. <span data-ttu-id="49fbf-109">Gå til **Transportstyring > Opsætning > Klassificering > Pausemaster**.</span><span class="sxs-lookup"><span data-stu-id="49fbf-109">Go to **Transportation management > Setup > Rating > Break master**.</span></span> <span data-ttu-id="49fbf-110">Pausemastere bruges til at definere prisstrukturen og dens pausepunkter.</span><span class="sxs-lookup"><span data-stu-id="49fbf-110">Break masters are used to define the pricing structure and its breakpoints.</span></span> <span data-ttu-id="49fbf-111">Prisstrukturen bruger lagdelte priser, der er baseret på fysiske dimensioner.</span><span class="sxs-lookup"><span data-stu-id="49fbf-111">The pricing structure uses tiered pricing that is based on physical dimensions.</span></span>  
1. <span data-ttu-id="49fbf-112">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="49fbf-112">Select **New**.</span></span>
1. <span data-ttu-id="49fbf-113">Indtast en værdi i feltet **Pausemaster**.</span><span class="sxs-lookup"><span data-stu-id="49fbf-113">In the **Break master** field, enter a value.</span></span>
1. <span data-ttu-id="49fbf-114">Angiv en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="49fbf-114">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="49fbf-115">Vælg datatypen i feltet **Datatype**.</span><span class="sxs-lookup"><span data-stu-id="49fbf-115">In the **Data type** field, select the data type.</span></span>
1. <span data-ttu-id="49fbf-116">I feltet **Sammenligning** skal du angive den type sammenligning, der ønskes (med operatorer).</span><span class="sxs-lookup"><span data-stu-id="49fbf-116">In the **Comparison** field, enter the kind of comparison requested (using operators).</span></span>
1. <span data-ttu-id="49fbf-117">Angiv pauseenheden i feltet **Afbryd enhed**.</span><span class="sxs-lookup"><span data-stu-id="49fbf-117">In the **Break unit** field, enter the break unit.</span></span>
1. <span data-ttu-id="49fbf-118">I **Detaljer**-sektionen kan du oprette så mange pauser, der er brug for til prissætningsstrukturen.</span><span class="sxs-lookup"><span data-stu-id="49fbf-118">In the **Details** section, create as many breaks as needed for the pricing structure.</span></span>
1. <span data-ttu-id="49fbf-119">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="49fbf-119">Select **Save**.</span></span>

## <a name="set-up-rate-master"></a><span data-ttu-id="49fbf-120">Konfigurer satsmaster</span><span class="sxs-lookup"><span data-stu-id="49fbf-120">Set up rate master</span></span>

1. <span data-ttu-id="49fbf-121">Gå til **Transportstyring > Opsætning > Klassificering > Satsmaster**.</span><span class="sxs-lookup"><span data-stu-id="49fbf-121">Go to **Transportation management > Setup > Rating > Rate master**.</span></span>
1. <span data-ttu-id="49fbf-122">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="49fbf-122">Select **New**.</span></span>
1. <span data-ttu-id="49fbf-123">Skriv en værdi i feltet **Satsmaster**.</span><span class="sxs-lookup"><span data-stu-id="49fbf-123">In the **Rate master** field, type a value.</span></span>
1. <span data-ttu-id="49fbf-124">Skriv en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="49fbf-124">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="49fbf-125">Vælg rullelistens knap i feltet **Vurderingsmetadata-id** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="49fbf-125">In the **Rating metadata ID** field, select the drop-down button to open the lookup.</span></span> <span data-ttu-id="49fbf-126">Vurderingsmetadata-id'et bestemmer de data, der er nødvendige for satsmasteren, da det definerer de metadata, der forventes af transportstyringsprogrammet, der bruger denne satsmaster.</span><span class="sxs-lookup"><span data-stu-id="49fbf-126">The rating metadata ID will determine the data needed for the rate master, as it defines the metadata expected by the transportation management engine using this rate master.</span></span>  
1. <span data-ttu-id="49fbf-127">Vælg P2P-indstillingen til dette eksempel.</span><span class="sxs-lookup"><span data-stu-id="49fbf-127">For this example, select the P2P option.</span></span> <span data-ttu-id="49fbf-128">Dette er allerede defineret i demodataene.</span><span class="sxs-lookup"><span data-stu-id="49fbf-128">This is already defined in the demo data.</span></span>
1. <span data-ttu-id="49fbf-129">Vælg linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="49fbf-129">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="49fbf-130">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="49fbf-130">Select **Save**.</span></span>

## <a name="set-up-rate-base"></a><span data-ttu-id="49fbf-131">Konfigurer satsgrundlag</span><span class="sxs-lookup"><span data-stu-id="49fbf-131">Set up rate base</span></span>

1. <span data-ttu-id="49fbf-132">Vælg **Satsgrundlag**.</span><span class="sxs-lookup"><span data-stu-id="49fbf-132">Select **Rate base**.</span></span>
    * <span data-ttu-id="49fbf-133">Satsgrundlaget bestemmer satsen for fragtmanden og kan bruges til at konfigurere en tarifstruktur, da den strukturerer satserne i pausepunkterne, der er defineret i pausemasteren.</span><span class="sxs-lookup"><span data-stu-id="49fbf-133">The rate base determines the rate of the carrier, and can be used to set up a tariff structure as it structures the rates in the breakpoints defined in the break master.</span></span>  
2. <span data-ttu-id="49fbf-134">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="49fbf-134">Select **New**.</span></span>
3. <span data-ttu-id="49fbf-135">Skriv en værdi i feltet **Satsgrundlag**.</span><span class="sxs-lookup"><span data-stu-id="49fbf-135">In the **Rate base** field, type a value.</span></span>
4. <span data-ttu-id="49fbf-136">Skriv en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="49fbf-136">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="49fbf-137">Vælg rullelistens knap i feltet **Pausemaster** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="49fbf-137">In the **Break master** field, select the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="49fbf-138">Pausemastere bruges til at definere prisstrukturen og dens pausepunkter.</span><span class="sxs-lookup"><span data-stu-id="49fbf-138">Break masters are used to define the pricing structure and its breakpoints.</span></span> <span data-ttu-id="49fbf-139">Prisstrukturen bruger lagdelte priser, der er baseret på fysiske dimensioner.</span><span class="sxs-lookup"><span data-stu-id="49fbf-139">The pricing structure uses tiered pricing that is based on physical dimensions.</span></span>  
6. <span data-ttu-id="49fbf-140">I dette eksempel skal du bruge vægt.</span><span class="sxs-lookup"><span data-stu-id="49fbf-140">For this example, use weight.</span></span> <span data-ttu-id="49fbf-141">Dette er allerede defineret i demodataene.</span><span class="sxs-lookup"><span data-stu-id="49fbf-141">This is already defined in the demo data.</span></span>
7. <span data-ttu-id="49fbf-142">Vælg linket i den fremhævede række på listen.</span><span class="sxs-lookup"><span data-stu-id="49fbf-142">In the list, select the link in the highlighted row.</span></span>
8. <span data-ttu-id="49fbf-143">Udvid afsnittet **Detaljer**.</span><span class="sxs-lookup"><span data-stu-id="49fbf-143">Expand the **Details** section.</span></span>
9. <span data-ttu-id="49fbf-144">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="49fbf-144">Select **New**.</span></span>
10. <span data-ttu-id="49fbf-145">Skriv "30301" i feltet **Postnummer på levering andet sted**.</span><span class="sxs-lookup"><span data-stu-id="49fbf-145">In the **Drop-off Postal Code From** field, type "30301".</span></span>
11. <span data-ttu-id="49fbf-146">Skriv "30318" i feltet **Til postnummer på levering andet sted**.</span><span class="sxs-lookup"><span data-stu-id="49fbf-146">In the **Drop-off Postal Code To** field, type "30318".</span></span>
12. <span data-ttu-id="49fbf-147">Skriv "USA" i feltet **Land/område for levering andet sted**.</span><span class="sxs-lookup"><span data-stu-id="49fbf-147">In the **Drop-off Country Region** field, type "USA".</span></span>
13. <span data-ttu-id="49fbf-148">Skriv "100" i feltet **<1.00 Lbs**.</span><span class="sxs-lookup"><span data-stu-id="49fbf-148">In the **<1.00 Lbs** field, type "100".</span></span>
    * <span data-ttu-id="49fbf-149">Indsæt satsen pr. pund, hvis den samlede vægt af lasten er mindre end 1 pund.</span><span class="sxs-lookup"><span data-stu-id="49fbf-149">Insert the rate per pounds if the total weight of the load is less than 1 pound.</span></span>  
14. <span data-ttu-id="49fbf-150">Skriv "300" i feltet **<5.00 Lbs**.</span><span class="sxs-lookup"><span data-stu-id="49fbf-150">In the **<5.00 Lbs** field, type "300".</span></span>
    * <span data-ttu-id="49fbf-151">Indsæt satsen pr. pund, hvis den samlede vægt af lasten er mindre end 5 pund.</span><span class="sxs-lookup"><span data-stu-id="49fbf-151">Insert the rate per pounds if the total weight of the load is less than 5 pounds.</span></span>  
15. <span data-ttu-id="49fbf-152">Skriv "500" i feltet **<20.00 Lbs**.</span><span class="sxs-lookup"><span data-stu-id="49fbf-152">In the **<20.00 Lbs** field, type "500".</span></span>
    * <span data-ttu-id="49fbf-153">Indsæt satsen pr. pund, hvis den samlede vægt af lasten er mindre end 20 pund.</span><span class="sxs-lookup"><span data-stu-id="49fbf-153">Insert the rate per pounds if the total weight of the load is less than 20 pounds.</span></span>  
16. <span data-ttu-id="49fbf-154">Skriv "1000" i feltet **<100.00 Lbs**.</span><span class="sxs-lookup"><span data-stu-id="49fbf-154">In the **<100.00 Lbs** field, type "1000".</span></span>
    * <span data-ttu-id="49fbf-155">Indsæt satsen pr. pund, hvis den samlede vægt af lasten er mindre end 100 pund.</span><span class="sxs-lookup"><span data-stu-id="49fbf-155">Insert the rate per pounds if the total weight of the load is less than 100 pounds.</span></span>  
17. <span data-ttu-id="49fbf-156">Skriv "3000" i feltet **<1,000.00 Lbs**.</span><span class="sxs-lookup"><span data-stu-id="49fbf-156">In the **<1,000.00 Lbs** field, type "3000".</span></span>
    * <span data-ttu-id="49fbf-157">Indsæt satsen pr. pund, hvis den samlede vægt af lasten er mindre end 1000 pund.</span><span class="sxs-lookup"><span data-stu-id="49fbf-157">Insert the rate per pounds if the total weight of the load is less than 1000 pounds.</span></span>  
18. <span data-ttu-id="49fbf-158">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="49fbf-158">Select **Save**.</span></span>
19. <span data-ttu-id="49fbf-159">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="49fbf-159">Close the page.</span></span>

## <a name="assign-rate-base"></a><span data-ttu-id="49fbf-160">Tildel satsgrundlag</span><span class="sxs-lookup"><span data-stu-id="49fbf-160">Assign rate base</span></span>

1. <span data-ttu-id="49fbf-161">Udvid sektionen **Tildelinger af satsgrundlag**.</span><span class="sxs-lookup"><span data-stu-id="49fbf-161">Expand the **Rate base assignments** section.</span></span>
2. <span data-ttu-id="49fbf-162">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="49fbf-162">Select **New**.</span></span>
    * <span data-ttu-id="49fbf-163">Du kan have flere tildelinger af satsgrundlag for hver satsmaster.</span><span class="sxs-lookup"><span data-stu-id="49fbf-163">You can have several rate base assignments for each rate master.</span></span> <span data-ttu-id="49fbf-164">Det gør det muligt at oprette flere forskellige prispointer for hver fragtmand afhængigt af destinationer, tjenester eller andre satsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="49fbf-164">This makes it possible to create several different price points for each carrier depending on destinations, services, or different rate bases.</span></span> <span data-ttu-id="49fbf-165">I denne procedure skal du kun oprette én satsbasistildeling.</span><span class="sxs-lookup"><span data-stu-id="49fbf-165">In this procedure you will only create one rate base assignment.</span></span>  
3. <span data-ttu-id="49fbf-166">Skriv en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="49fbf-166">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="49fbf-167">Klik på rullelistens knap i feltet **Satsgrundlag** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="49fbf-167">In the **Rate base** field, select the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="49fbf-168">Vælg linket i den fremhævede række på listen.</span><span class="sxs-lookup"><span data-stu-id="49fbf-168">In the list, select the link in the highlighted row.</span></span>
6. <span data-ttu-id="49fbf-169">Vælg rullelistens knap i feltet **Service** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="49fbf-169">In the **Service** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="49fbf-170">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="49fbf-170">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="49fbf-171">Vælg linket i den fremhævede række på listen.</span><span class="sxs-lookup"><span data-stu-id="49fbf-171">In the list, select the link in the highlighted row.</span></span>
9. <span data-ttu-id="49fbf-172">Skriv "98052" i feltet **Postnummer på afhentning**.</span><span class="sxs-lookup"><span data-stu-id="49fbf-172">In the **Pick-up Postal Code** field, type "98052".</span></span>
    * <span data-ttu-id="49fbf-173">Angiv, hvilket postnummer denne satsbasistildeling skal være gyldig fra.</span><span class="sxs-lookup"><span data-stu-id="49fbf-173">Specify which postal code this rate base assignment should be valid from.</span></span>
10. <span data-ttu-id="49fbf-174">Skriv "USA" i feltet **Afhentningsland/område**.</span><span class="sxs-lookup"><span data-stu-id="49fbf-174">In the **Pick-up Country Region** field, type "USA".</span></span>
11. <span data-ttu-id="49fbf-175">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="49fbf-175">Select **Save**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]