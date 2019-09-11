---
title: Definere cyklusoptælling
description: Cyklusoptælling er en lagerproces, du kan bruge til at overvåge disponible varer i lagerbeholdningen.
author: MarkusFogelberg
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 24c4c27745a15f013d20b52efc6e36de848a0251
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916777"
---
# <a name="define-cycle-counting"></a><span data-ttu-id="71a3c-103">Definere cyklusoptælling</span><span class="sxs-lookup"><span data-stu-id="71a3c-103">Define cycle counting</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="71a3c-104">Cyklusoptælling er en lagerproces, du kan bruge til at overvåge disponible varer i lagerbeholdningen.</span><span class="sxs-lookup"><span data-stu-id="71a3c-104">Cycle counting is a warehouse process that you can use to audit on-hand inventory items.</span></span> <span data-ttu-id="71a3c-105">Denne opgave viser, hvordan du: opsætter standardoptælling af arbejdsprioritet, aktiverer et mobilenhedsmenupunkt til at behandle både plukning og optælling, aktiverer en udløser for optællingsgrænse, når en placering bliver tom, og aktiverer en cyklusoptællingsplan for et bestemt element i et bestemt lagersted.</span><span class="sxs-lookup"><span data-stu-id="71a3c-105">This task recording shows how to set up the default counting work priority, enable a mobile device menu item to process both picking and counting operations, enable a counting threshold trigger when a location becomes empty, and enable a cycle counting plan for a specific item in a specific warehouse.</span></span> <span data-ttu-id="71a3c-106">Disse opgaver udføres typisk af en lagerstedschef.</span><span class="sxs-lookup"><span data-stu-id="71a3c-106">Typically, these tasks are performed by a warehouse manager.</span></span> <span data-ttu-id="71a3c-107">Du kan gennemgå denne procedure i USMF-demodatafirmaet eller i dine egne data.</span><span class="sxs-lookup"><span data-stu-id="71a3c-107">You can go through this procedure in the USMF demo data company or in your own data.</span></span>


## <a name="set-the-priority-of-counting-work"></a><span data-ttu-id="71a3c-108">Angive prioriteten for optælling af arbejde</span><span class="sxs-lookup"><span data-stu-id="71a3c-108">Set the priority of counting work</span></span>
1. <span data-ttu-id="71a3c-109">I **navigationsruden** skal du gå til **Moduler > Lokationsstyring > Opsætning > Parametre til lokationsstyring**.</span><span class="sxs-lookup"><span data-stu-id="71a3c-109">In the **Navigation pane**, go to **Modules > Warehouse management > Setup > Warehouse management parameters**.</span></span>
2. <span data-ttu-id="71a3c-110">Klik på fanen **Cyklusoptælling**.</span><span class="sxs-lookup"><span data-stu-id="71a3c-110">Click the **Cycle counting** tab.</span></span>
3. <span data-ttu-id="71a3c-111">Skriv et tal i feltet **Prioritet for standardcyklusoptællingsarbejde**.</span><span class="sxs-lookup"><span data-stu-id="71a3c-111">In the **Default cycle count work priority** field, enter a number.</span></span> <span data-ttu-id="71a3c-112">Dette trin ændrer prioriteten af cyklusoptællingsarbejdet sammenlignet med andre typer af arbejde på lageret.</span><span class="sxs-lookup"><span data-stu-id="71a3c-112">This step changes the priority of cycle counting work compared to other types of work in the warehouse.</span></span> <span data-ttu-id="71a3c-113">Du kan øge prioriteten af cyklusoptællingsarbejde ved at angive et lavere tal end for andre typer arbejde.</span><span class="sxs-lookup"><span data-stu-id="71a3c-113">By entering a number that is lower than the number for other types of work, you raise the priority of the cycle counting work.</span></span>  
4. <span data-ttu-id="71a3c-114">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="71a3c-114">Click **Save**.</span></span>
5. <span data-ttu-id="71a3c-115">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="71a3c-115">Close the page.</span></span>

## <a name="enable-the-mobile-device"></a><span data-ttu-id="71a3c-116">Aktivere mobilenheden</span><span class="sxs-lookup"><span data-stu-id="71a3c-116">Enable the mobile device</span></span>
1. <span data-ttu-id="71a3c-117">Gå i **navigationsruden** til **Moduler > Lokationsstyring > Opsætning > Mobilenhed > Menupunkter i mobilenhed**.</span><span class="sxs-lookup"><span data-stu-id="71a3c-117">In the **Navigation pane**, go to **Modules > Warehouse management > Setup > Mobile device > Mobile device menu items**.</span></span>
2. <span data-ttu-id="71a3c-118">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="71a3c-118">Click **New**.</span></span>
3. <span data-ttu-id="71a3c-119">Skriv en værdi i feltet **Menupunktnavn**.</span><span class="sxs-lookup"><span data-stu-id="71a3c-119">In the **Menu item name** field, type a value.</span></span>
4. <span data-ttu-id="71a3c-120">Skriv en værdi i feltet **Titel**.</span><span class="sxs-lookup"><span data-stu-id="71a3c-120">In the **Title** field, type a value.</span></span>
5. <span data-ttu-id="71a3c-121">Vælg 'Arbejde' i feltet **Tilstand**.</span><span class="sxs-lookup"><span data-stu-id="71a3c-121">In the **Mode** field, select 'Work'.</span></span>
6. <span data-ttu-id="71a3c-122">Angiv indstillingen **Brug eksisterende arbejde** til Ja.</span><span class="sxs-lookup"><span data-stu-id="71a3c-122">Set the **Use existing work** option to Yes.</span></span> <span data-ttu-id="71a3c-123">Når du vælger Ja for denne indstilling, søger systemet efter eksisterende arbejde, når mobilenhedsmenupunktet bruges.</span><span class="sxs-lookup"><span data-stu-id="71a3c-123">When you set this option to Yes, the system will look for existing work when the mobile device menu item is used.</span></span>  
7. <span data-ttu-id="71a3c-124">Vælg 'Systembaseret' i feltet **Ledet af**.</span><span class="sxs-lookup"><span data-stu-id="71a3c-124">In the **Directed by** field, select 'System directed'.</span></span> <span data-ttu-id="71a3c-125">Når Systembaseret er markeret, føres lagermedarbejderen til det åbne arbejde, der er defineret i arbejdsklasser.</span><span class="sxs-lookup"><span data-stu-id="71a3c-125">When "System directed" is selected, the warehouse worker will be directed to open work that is in defined work classes.</span></span> <span data-ttu-id="71a3c-126">(Vi vil oprette disse arbejdsklasser som det næste).</span><span class="sxs-lookup"><span data-stu-id="71a3c-126">(We will create these work classes next.)</span></span>  
8. <span data-ttu-id="71a3c-127">Udvid oversigtspanelet **Arbejdsklasser**.</span><span class="sxs-lookup"><span data-stu-id="71a3c-127">Expand the **Work classes** fastTab.</span></span> <span data-ttu-id="71a3c-128">Nu skal vi oprette to arbejdsklasser, der skal bruges sammen med dette menupunkt på mobilenheden.</span><span class="sxs-lookup"><span data-stu-id="71a3c-128">Next, we will create two work classes that will be used with this mobile device menu item.</span></span> <span data-ttu-id="71a3c-129">Når dette menupunkt bruges, forespørges der på disse arbejdsklasser, og det arbejdet, der har den højeste prioritet, vises for brugeren.</span><span class="sxs-lookup"><span data-stu-id="71a3c-129">When the menu item is used, these work classes will be queried, and the work that has the highest priority will be shown to the user.</span></span>  
9. <span data-ttu-id="71a3c-130">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="71a3c-130">Click **New**.</span></span>
10. <span data-ttu-id="71a3c-131">Vælg en værdi i feltet **Arbejdsklasse-id**.</span><span class="sxs-lookup"><span data-stu-id="71a3c-131">In the**Work class ID** field, select a value.</span></span>
11. <span data-ttu-id="71a3c-132">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="71a3c-132">Click **New**.</span></span>
12. <span data-ttu-id="71a3c-133">Vælg en værdi i feltet **Arbejdsklasse-id**.</span><span class="sxs-lookup"><span data-stu-id="71a3c-133">In the **Work class ID** field, select a value.</span></span>
13. <span data-ttu-id="71a3c-134">Klik på **Gem** i **handlingsruden**.</span><span class="sxs-lookup"><span data-stu-id="71a3c-134">In the **Action pane**, click **Save**.</span></span>
14. <span data-ttu-id="71a3c-135">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="71a3c-135">Close the page.</span></span>
15. <span data-ttu-id="71a3c-136">Gå i **navigationsruden** til **Moduler > Lokationsstyring > Opsætning > Mobilenhed > Menu i mobilenhed**.</span><span class="sxs-lookup"><span data-stu-id="71a3c-136">In the **Navigation pane**, go to **Modules > Warehouse management > Setup > Mobile device > Mobile device menu**.</span></span>
16. <span data-ttu-id="71a3c-137">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="71a3c-137">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="71a3c-138">Vælg 'det menupunkt, du lige har oprettet' i træet.</span><span class="sxs-lookup"><span data-stu-id="71a3c-138">In the tree, select 'the menu item that you just created'.</span></span>
18. <span data-ttu-id="71a3c-139">Klik på **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="71a3c-139">Click **Edit**.</span></span>
19. <span data-ttu-id="71a3c-140">Klik på pilen for at tilføje menupunktet til menuen.</span><span class="sxs-lookup"><span data-stu-id="71a3c-140">Click the arrow to add the menu item to the menu.</span></span>
20. <span data-ttu-id="71a3c-141">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="71a3c-141">Click **Save**.</span></span>

## <a name="create-a-counting-threshold"></a><span data-ttu-id="71a3c-142">Oprette en optællingsgrænse</span><span class="sxs-lookup"><span data-stu-id="71a3c-142">Create a counting threshold</span></span>
1. <span data-ttu-id="71a3c-143">Gå i **navigationsruden** til **Moduler > Lokationsstyring > Opsætning > Cyklusoptælling > Cyklusoptællingsgrænser**.</span><span class="sxs-lookup"><span data-stu-id="71a3c-143">In the **Navigation pane**, go to **Modules > Warehouse management > Setup > Cycle counting > Cycle count thresholds**.</span></span>
2. <span data-ttu-id="71a3c-144">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="71a3c-144">Click **New**.</span></span>
3. <span data-ttu-id="71a3c-145">Skriv en værdi i feltet **Id for cyklusoptællingsgrænse**.</span><span class="sxs-lookup"><span data-stu-id="71a3c-145">In the **Cycle counting threshold ID** field, type a value.</span></span>
4. <span data-ttu-id="71a3c-146">Angiv indstillingen **Udfør behandling af cyklusoptælling med det samme** til Ja.</span><span class="sxs-lookup"><span data-stu-id="71a3c-146">Set the **Process cycle counting immediately** option to Yes.</span></span>
5. <span data-ttu-id="71a3c-147">Indtast en værdi i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="71a3c-147">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="71a3c-148">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="71a3c-148">Click **Save**.</span></span>
7. <span data-ttu-id="71a3c-149">Klik på **Vælg lokationer**.</span><span class="sxs-lookup"><span data-stu-id="71a3c-149">Click **Select locations**.</span></span>
8. <span data-ttu-id="71a3c-150">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="71a3c-150">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="71a3c-151">Vælg en værdi i feltet **Kriterier**.</span><span class="sxs-lookup"><span data-stu-id="71a3c-151">In the **Criteria** field, select a value.</span></span>
10. <span data-ttu-id="71a3c-152">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="71a3c-152">Click **OK**.</span></span>
11. <span data-ttu-id="71a3c-153">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="71a3c-153">Close the page.</span></span>

## <a name="create-a-cycle-count-plan"></a><span data-ttu-id="71a3c-154">Oprette en cyklusoptællingsplan</span><span class="sxs-lookup"><span data-stu-id="71a3c-154">Create a cycle count plan</span></span>
1. <span data-ttu-id="71a3c-155">Gå i **navigationsruden** til **Moduler > Lokationsstyring > Opsætning > Cyklusoptælling > Cyklusoptællingsplaner**.</span><span class="sxs-lookup"><span data-stu-id="71a3c-155">In the **Navigation pane**, go to **Modules > Warehouse management > Setup > Cycle counting > Cycle count plans**.</span></span>
2. <span data-ttu-id="71a3c-156">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="71a3c-156">Click **New**.</span></span>
3. <span data-ttu-id="71a3c-157">Skriv en værdi i feltet **Id for cyklusoptællingsplan**.</span><span class="sxs-lookup"><span data-stu-id="71a3c-157">In the **Cycle counting plan ID** field, type a value.</span></span>
4. <span data-ttu-id="71a3c-158">Indtast en værdi i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="71a3c-158">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="71a3c-159">Angiv et tal i feltet **Maks. antal cyklusoptællinger**.</span><span class="sxs-lookup"><span data-stu-id="71a3c-159">In the **Maximum number of cycle counts** field, enter a number.</span></span>
6. <span data-ttu-id="71a3c-160">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="71a3c-160">Click **Save**.</span></span>
7. <span data-ttu-id="71a3c-161">Klik på **Vælg lokationer**.</span><span class="sxs-lookup"><span data-stu-id="71a3c-161">Click **Select locations**.</span></span>
8. <span data-ttu-id="71a3c-162">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="71a3c-162">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="71a3c-163">Vælg en værdi i feltet **Kriterier**.</span><span class="sxs-lookup"><span data-stu-id="71a3c-163">In the **Criteria** field, select a value.</span></span>
10. <span data-ttu-id="71a3c-164">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="71a3c-164">Click **OK**.</span></span>
11. <span data-ttu-id="71a3c-165">Skriv et tal i feltet **Dage mellem cyklusoptællinger**.</span><span class="sxs-lookup"><span data-stu-id="71a3c-165">In the **Days between cycle counting** field, enter a number.</span></span> <span data-ttu-id="71a3c-166">Hvis f.eks. antallet i feltet **Dage mellem cyklusoptællinger**, er indstillet til 5, oprettes der cyklusoptællingsarbejde, hver gang der er gået fem dage.</span><span class="sxs-lookup"><span data-stu-id="71a3c-166">For example, if the **Days between cycle counting** field is set to 5, cycle counting work will be created every five days.</span></span> <span data-ttu-id="71a3c-167">Men cyklusoptællingsarbejdet imidlertid behandles på dag tre, oprettes det næste cyklusoptællingsarbejde, fem dage efter at den seneste cyklusoptælling blev behandling, nemlig på dag 8.</span><span class="sxs-lookup"><span data-stu-id="71a3c-167">However, if cycle counting work is processed on day three, the next cycle counting work will be created five days after the last cycle counting was processed, on day 8.</span></span>  
12. <span data-ttu-id="71a3c-168">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="71a3c-168">Click **Save**.</span></span>
13. <span data-ttu-id="71a3c-169">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="71a3c-169">Click **New**.</span></span>
14. <span data-ttu-id="71a3c-170">Indtast et tal i feltet **Serienummer**.</span><span class="sxs-lookup"><span data-stu-id="71a3c-170">In the **Sequence number** field, enter a number.</span></span> <span data-ttu-id="71a3c-171">Sorteringen udføres fra det mindste tal til det største tal.</span><span class="sxs-lookup"><span data-stu-id="71a3c-171">The sort is from the smallest number to the largest number.</span></span> <span data-ttu-id="71a3c-172">Værdien skal være større end 0 (nul).</span><span class="sxs-lookup"><span data-stu-id="71a3c-172">The value must be more than 0 (zero).</span></span>  
15. <span data-ttu-id="71a3c-173">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="71a3c-173">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="71a3c-174">Indtast en værdi i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="71a3c-174">In the **Description** field, type a value.</span></span>
17. <span data-ttu-id="71a3c-175">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="71a3c-175">Click **Save**.</span></span>
18. <span data-ttu-id="71a3c-176">Klik på **Definer produktforespørgsel**.</span><span class="sxs-lookup"><span data-stu-id="71a3c-176">Click **Define product** query.</span></span>
19. <span data-ttu-id="71a3c-177">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="71a3c-177">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="71a3c-178">Indtast eller vælg en værdi i feltet **Kriterier**.</span><span class="sxs-lookup"><span data-stu-id="71a3c-178">In the **Criteria** field, enter or select a value.</span></span>
21. <span data-ttu-id="71a3c-179">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="71a3c-179">Click **OK**.</span></span>
22. <span data-ttu-id="71a3c-180">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="71a3c-180">Close the page.</span></span>

