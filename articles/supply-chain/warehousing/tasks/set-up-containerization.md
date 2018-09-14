--- 
title: Konfigurere containerlogik
description: Denne procedure beskriver, hvordan du automatiserer containeriseringen af laster i Lagerstedsstyring.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 56fc6adc2a0eeb5b824089ff4b1b781f3a99a34c
ms.contentlocale: da-dk
ms.lasthandoff: 09/14/2018

---
# <a name="set-up-containerization"></a><span data-ttu-id="3d6ab-103">Konfigurere containerlogik</span><span class="sxs-lookup"><span data-stu-id="3d6ab-103">Set up containerization</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3d6ab-104">Denne procedure beskriver, hvordan du automatiserer containeriseringen af laster i Lagerstedsstyring.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-104">This procedure describes how to automate the containerization of loads in Warehouse management.</span></span> <span data-ttu-id="3d6ab-105">Automatiseret containerisering opretter containere og plukker arbejde for leverancer, når en bølge behandles og arbejdslinjer kan opdeles i mængder, der passer til containerne.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-105">Automated containerization creates containers and the picking work for shipments when a wave is processed and work lines can be split into quantities that fit the containers.</span></span> <span data-ttu-id="3d6ab-106">Det gør det lettere for lagermedarbejdere at plukke varer direkte i den valgte container.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-106">This helps warehouse workers to pick the items directly into the chosen container.</span></span> <span data-ttu-id="3d6ab-107">Sammenlignet med den manuelle pakningsproces, udføres opgaver såsom oprettelse af containere, tildeleling af varer og lukning af containere automatisk af systemet.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-107">Compared to the manual packing process, tasks such as creating containers, assigning items, and closing containers are automated by the system.</span></span> <span data-ttu-id="3d6ab-108">Denne procedure bruger USMF-demofirmaet og udføres af en lagerchef.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-108">This procedure uses the USMF demo company and is performed by a Warehouse manager.</span></span>


## <a name="set-up-a-wave-template"></a><span data-ttu-id="3d6ab-109">Konfigurere en bølgeskabelon</span><span class="sxs-lookup"><span data-stu-id="3d6ab-109">Set up a wave template</span></span>
1. <span data-ttu-id="3d6ab-110">Gå til Lagerstedsstyring > Konfiguration > Bølger > Bølgeskabeloner.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-110">Go to Warehouse management > Setup > Waves > Wave templates.</span></span>
2. <span data-ttu-id="3d6ab-111">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-111">Click New.</span></span>
3. <span data-ttu-id="3d6ab-112">Skriv en værdi i feltet Bølgeskabelonnavn.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-112">In the Wave template name field, type a value.</span></span>
4. <span data-ttu-id="3d6ab-113">Skriv en værdi i feltet Beskrivelse af bølgeskabelon.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-113">In the Wave template description field, type a value.</span></span>
5. <span data-ttu-id="3d6ab-114">Indtast eller vælg en værdi i feltet Lokation.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-114">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="3d6ab-115">Indtast eller vælg en værdi i feltet Lagersted.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-115">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="3d6ab-116">Udvid sektionen Metoder.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-116">Expand the Methods section.</span></span>
    * <span data-ttu-id="3d6ab-117">I vinduet Valgte metoder vises metoderne for den valgte bølgeskabelontype.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-117">The Selected methods pane lists the methods for the selected wave template type.</span></span> <span data-ttu-id="3d6ab-118">Bølgeskabelonen skal indeholde containeriseringsmetoden.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-118">The wave template must include the containerize method.</span></span>  
8. <span data-ttu-id="3d6ab-119">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-119">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="3d6ab-120">Skriv en værdi i feltet Kode for bølgetrin.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-120">In the Wave step code field, type a value.</span></span>
    * <span data-ttu-id="3d6ab-121">Angiv en bølgetrinkode for den tilføjede metode, som kan være en hvilken som helst kode.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-121">Enter a Wave step code for the added method, which can be any code.</span></span> <span data-ttu-id="3d6ab-122">Det er muligt at tilføje metoden mere end én gang og tildele forskellige bølgetrinkoder.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-122">It’s possible to add the method more than once and assign different wave step codes.</span></span> <span data-ttu-id="3d6ab-123">Til dette formål skal du vælge Kan gentages for denne metode på siden Metoder til bølgeproces.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-123">To do this, select Repeatable for this method in the Wave process methods page.</span></span>  
10. <span data-ttu-id="3d6ab-124">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-124">Click Save.</span></span>
11. <span data-ttu-id="3d6ab-125">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-125">Close the page.</span></span>

## <a name="set-up-a-container-type"></a><span data-ttu-id="3d6ab-126">Konfigurere en containertype</span><span class="sxs-lookup"><span data-stu-id="3d6ab-126">Set up a container type</span></span>
1. <span data-ttu-id="3d6ab-127">Gå til Lagerstedsstyring > Konfiguration > Containere > Containertyper.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-127">Go to Warehouse management > Setup > Containers > Container types.</span></span>
    * <span data-ttu-id="3d6ab-128">Du kan definere dine containere på siden Containertyper.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-128">You can define your containers in the Container types page.</span></span> <span data-ttu-id="3d6ab-129">Du kan konfiguree containeres fysiske dimensioner, herunder taravægt, maksimal vægt, maksimal volumen, længde, bredde, vægt og højde.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-129">You can configure the physical dimensions of containers including tare weight, maximum weight, maximum volume, length, width, and height.</span></span> <span data-ttu-id="3d6ab-130">I dette eksempel har vi tre forskellige størrelser af bokse.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-130">In this example, we have three different sizes of boxes.</span></span>  
2. <span data-ttu-id="3d6ab-131">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-131">Click New.</span></span>
3. <span data-ttu-id="3d6ab-132">Indtast en værdi i feltet Containertypekode.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-132">In the Container type code field, type a value.</span></span>
4. <span data-ttu-id="3d6ab-133">Angiv et tal i feltet Taravægt.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-133">In the Tare weight field, enter a number.</span></span>
5. <span data-ttu-id="3d6ab-134">Angiv et tal i feltet Maksimal vægt.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-134">In the Maximum weight field, enter a number.</span></span>
6. <span data-ttu-id="3d6ab-135">Angiv et tal i feltet Volumen.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-135">In the Volume field, enter a number.</span></span>
7. <span data-ttu-id="3d6ab-136">Angiv et tal i feltet Længde.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-136">In the Length field, enter a number.</span></span>
8. <span data-ttu-id="3d6ab-137">Indtast et tal i feltet Bredde.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-137">In the Width field, enter a number.</span></span>
9. <span data-ttu-id="3d6ab-138">Indtast et tal i feltet Højde.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-138">In the Height field, enter a number.</span></span>
10. <span data-ttu-id="3d6ab-139">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-139">In the Description field, type a value.</span></span>
11. <span data-ttu-id="3d6ab-140">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-140">Click Save.</span></span>
12. <span data-ttu-id="3d6ab-141">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-141">Click New.</span></span>
13. <span data-ttu-id="3d6ab-142">Indtast en værdi i feltet Containertypekode.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-142">In the Container type code field, type a value.</span></span>
14. <span data-ttu-id="3d6ab-143">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-143">In the Description field, type a value.</span></span>
15. <span data-ttu-id="3d6ab-144">Angiv et tal i feltet Taravægt.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-144">In the Tare weight field, enter a number.</span></span>
16. <span data-ttu-id="3d6ab-145">Angiv et tal i feltet Maksimal vægt.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-145">In the Maximum weight field, enter a number.</span></span>
17. <span data-ttu-id="3d6ab-146">Angiv et tal i feltet Volumen.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-146">In the Volume field, enter a number.</span></span>
18. <span data-ttu-id="3d6ab-147">Angiv et tal i feltet Længde.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-147">In the Length field, enter a number.</span></span>
19. <span data-ttu-id="3d6ab-148">Indtast et tal i feltet Bredde.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-148">In the Width field, enter a number.</span></span>
20. <span data-ttu-id="3d6ab-149">Indtast et tal i feltet Højde.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-149">In the Height field, enter a number.</span></span>
21. <span data-ttu-id="3d6ab-150">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-150">Click Save.</span></span>
22. <span data-ttu-id="3d6ab-151">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-151">Click New.</span></span>
23. <span data-ttu-id="3d6ab-152">Indtast en værdi i feltet Containertypekode.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-152">In the Container type code field, type a value.</span></span>
24. <span data-ttu-id="3d6ab-153">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-153">In the Description field, type a value.</span></span>
25. <span data-ttu-id="3d6ab-154">Angiv et tal i feltet Taravægt.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-154">In the Tare weight field, enter a number.</span></span>
26. <span data-ttu-id="3d6ab-155">Angiv et tal i feltet Maksimal vægt.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-155">In the Maximum weight field, enter a number.</span></span>
27. <span data-ttu-id="3d6ab-156">Angiv et tal i feltet Volumen.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-156">In the Volume field, enter a number.</span></span>
28. <span data-ttu-id="3d6ab-157">Angiv et tal i feltet Længde.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-157">In the Length field, enter a number.</span></span>
29. <span data-ttu-id="3d6ab-158">Indtast et tal i feltet Bredde.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-158">In the Width field, enter a number.</span></span>
30. <span data-ttu-id="3d6ab-159">Indtast et tal i feltet Højde.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-159">In the Height field, enter a number.</span></span>
31. <span data-ttu-id="3d6ab-160">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-160">Click Save.</span></span>
32. <span data-ttu-id="3d6ab-161">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-161">Close the page.</span></span>

## <a name="set-up-a-container-group"></a><span data-ttu-id="3d6ab-162">Konfigurere en containergruppe</span><span class="sxs-lookup"><span data-stu-id="3d6ab-162">Set up a container group</span></span>
1. <span data-ttu-id="3d6ab-163">Gå til Lagerstedsstyring > Konfiguration > Containere > Containergrupper.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-163">Go to Warehouse management > Setup > Containers > Container groups.</span></span>
2. <span data-ttu-id="3d6ab-164">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-164">Click New.</span></span>
    * <span data-ttu-id="3d6ab-165">Du kan konfigurere logiske grupper af containertyper.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-165">You can set up logical groups of container types.</span></span> <span data-ttu-id="3d6ab-166">For hver gruppe kan du angive den rækkefølge, i hvilken du skal pakke containerne, og hvor meget containerne skal fyldes op i procent. Varens størrelsesdimensioner bruges til at bestemme, om den kan være i en container.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-166">For each group, you can specify the sequence in which to pack the containers and the percentage of the containers to fill.The size dimensions of the item is used to determine whether it will fit in a container.</span></span> <span data-ttu-id="3d6ab-167">Den container, der er tættest på varens størrelsesdimension, bruges.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-167">The container that is closest to the size dimensions of the item is used.</span></span> <span data-ttu-id="3d6ab-168">Hvis du har flere containertyper i en gruppe, anbefaler vi, at du arrangerer rækkefølgen efter størrelse, så den største container er først, nummer 1 i rækkefølgen, og den mindste container er sidst.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-168">If you have multiple container types in a group, we recommend that you arrange the sequence by size, so that the largest container is first, number 1 in the sequence, and the smallest container is last.</span></span>    
3. <span data-ttu-id="3d6ab-169">Skriv en værdi i feltet Containergruppe-id.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-169">In the Container group ID field, type a value.</span></span>
4. <span data-ttu-id="3d6ab-170">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-170">In the Description field, type a value.</span></span>
5. <span data-ttu-id="3d6ab-171">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-171">Click New.</span></span>
6. <span data-ttu-id="3d6ab-172">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-172">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="3d6ab-173">Indtast eller vælg en værdi i feltet Containertype.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-173">In the Container type field, enter or select a value.</span></span>
8. <span data-ttu-id="3d6ab-174">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-174">Click New.</span></span>
9. <span data-ttu-id="3d6ab-175">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-175">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="3d6ab-176">Indtast eller vælg en værdi i feltet Containertype.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-176">In the Container type field, enter or select a value.</span></span>
11. <span data-ttu-id="3d6ab-177">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-177">Click New.</span></span>
12. <span data-ttu-id="3d6ab-178">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-178">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="3d6ab-179">Indtast eller vælg en værdi i feltet Containertype.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-179">In the Container type field, enter or select a value.</span></span>
14. <span data-ttu-id="3d6ab-180">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-180">Click Save.</span></span>
15. <span data-ttu-id="3d6ab-181">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-181">Close the page.</span></span>

## <a name="set-up-a-container-build-template"></a><span data-ttu-id="3d6ab-182">Konfigurere en containerbuildskabelon</span><span class="sxs-lookup"><span data-stu-id="3d6ab-182">Set up a container build template</span></span>
1. <span data-ttu-id="3d6ab-183">Gå til Lagerstedsstyring > Konfiguration > Containere > Skabeloner til container-build.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-183">Go to Warehouse management > Setup > Containers > Container build templates.</span></span>
2. <span data-ttu-id="3d6ab-184">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-184">Click New.</span></span>
    * <span data-ttu-id="3d6ab-185">Skabelonen til container-build er baseret på, hvilke af containeriseringsprocesserne der udføres.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-185">The container build template is based on which of the containerization processes are performed.</span></span> <span data-ttu-id="3d6ab-186">Hver skabelon til container-build definerer en containeriseringsproces, der vil blive brugt af en bølgeskabelon.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-186">Each container build template defines one containerization process that will be used by a wave template.</span></span> <span data-ttu-id="3d6ab-187">Indstillingen Rediger forespørgsel giver dig mulighed at definere de betingelser, som den valgte skabelon vil blive behandlet under.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-187">The Edit query option allows you to define the conditions on which the selected template will be processed.</span></span> <span data-ttu-id="3d6ab-188">For eksempel kan du kun køre containerisering for bestemte kunder, produkter eller lagersteder, eller du kan tilføje de tilsvarende forespørgselsområder til skabelonen.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-188">For example, you may want to only run containerization for specific customers, products, or warehouses or you can add the corresponding query ranges to the template.</span></span> <span data-ttu-id="3d6ab-189">Feltet Bølgetrinkode viser, hvordan en skabelon til container-build er knyttet til trinnene i en bølgeskabelon.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-189">The Wave step code field is how a container build template is linked to steps in a wave template.</span></span> <span data-ttu-id="3d6ab-190">Når der udføres en bølge, bestemmer den, hvilke skabeloner til container-build der bruges til at starte containeriseringen.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-190">When a wave is executed, it determines which container build template(s) are used to initiate containerization.</span></span> <span data-ttu-id="3d6ab-191">Feltet Basisforespørgselstype bestemmer, hvad der skal pakkes, og hvad filterforespørgslen skal baseres på.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-191">The Base query type field determines what to pack and what to base the filter query on.</span></span>  
3. <span data-ttu-id="3d6ab-192">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-192">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="3d6ab-193">Skriv en værdi i feltet Containerskabelon-id.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-193">In the Container template ID field, type a value.</span></span>
5. <span data-ttu-id="3d6ab-194">Indtast eller vælg en værdi i feltet Containergruppe-id.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-194">In the Container group ID field, enter or select a value.</span></span>
6. <span data-ttu-id="3d6ab-195">Skriv en værdi i feltet Kode for bølgetrin.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-195">In the Wave step code field, type a value.</span></span>
7. <span data-ttu-id="3d6ab-196">Markér afkrydsningsfeltet Tillad opdeling af plukninger.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-196">Select the Allow split picks check box.</span></span>
8. <span data-ttu-id="3d6ab-197">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-197">Click Save.</span></span>
9. <span data-ttu-id="3d6ab-198">Klik på Begrænsninger i containerblanding.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-198">Click Containier mixing constraints.</span></span>
    * <span data-ttu-id="3d6ab-199">Med pauser i blandingsregler kan du angive regler for fordelingslinjer for pakning i containere.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-199">Mixing logic breaks allows you to set up rules for packing allocation lines in containers.</span></span> <span data-ttu-id="3d6ab-200">Hvis du for eksempel tilføjer feltet Varenummer, når varer tildeles containere, oprettes der en ny container, når der er et nyt varenummer.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-200">For example, if you add the Item number field, when items are assigned to containers, a new container will be created when there is a new item number.</span></span> <span data-ttu-id="3d6ab-201">Dette er vil forhindre, at arbejdere pakker fordelingslinjer for to forskellige kunder i samme container.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-201">This is will prevent workers from packing allocations lines for two different customers in the same container.</span></span>  
10. <span data-ttu-id="3d6ab-202">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-202">Click New.</span></span>
11. <span data-ttu-id="3d6ab-203">Vælg en indstilling i feltet Tabel.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-203">In the Table field, select an option.</span></span>
12. <span data-ttu-id="3d6ab-204">Indtast eller vælg en værdi i feltet Valg af felt.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-204">In the Field Select field, enter or select a value.</span></span>
13. <span data-ttu-id="3d6ab-205">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="3d6ab-205">Click OK.</span></span>


