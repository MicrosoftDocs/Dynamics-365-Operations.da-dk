---
title: Pluklinjegruppering
description: Dette emne indeholder en oversigt over pluklinjegruppering.
author: Mirzaab
manager: tfehr
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 4b9cd7dac680c1691fb4c6dd4078f109254be784
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215587"
---
# <a name="pick-line-grouping"></a><span data-ttu-id="0fb53-103">Pluklinjegruppering</span><span class="sxs-lookup"><span data-stu-id="0fb53-103">Pick line grouping</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0fb53-104">I pluklinjegruppering kan flere arbejdslinjer, der har samme vare og lokation, kombineres til et enkelt pluk, der præsenteres for brugeren på en mobilenhed.</span><span class="sxs-lookup"><span data-stu-id="0fb53-104">In pick line grouping, multiple work lines that have the same item and location can be combined into a single pick that is presented to the user on a mobile device.</span></span> <span data-ttu-id="0fb53-105">Derfor kan lagermedarbejderne modtage de mest mulige effektive instruktioner, men den påkrævede adskillelse af arbejdslinjer i systemet bibeholdes ligeså (f.eks. for forskellige containere og ordrer).</span><span class="sxs-lookup"><span data-stu-id="0fb53-105">Therefore, warehouse workers can receive the most efficient instructions that are possible, but the required separation of work lines in the system is also maintained (for example, for different containers and orders).</span></span>

## <a name="set-up-pick-line-grouping"></a><span data-ttu-id="0fb53-106">Opsætning af pluklinjegruppering</span><span class="sxs-lookup"><span data-stu-id="0fb53-106">Set up pick line grouping</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="0fb53-107">Oprette et menupunkt på en mobilenhed</span><span class="sxs-lookup"><span data-stu-id="0fb53-107">Create a mobile device menu item</span></span>

1. <span data-ttu-id="0fb53-108">Gå til **Lokationsstyring \> Opsætning \> Mobilenhed \> Mobilenhedsmenupunkter**, og opret et nyt menupunkt kaldet **Salgsgruppelinjepluk – brugerstyret**.</span><span class="sxs-lookup"><span data-stu-id="0fb53-108">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**, and create a new menu item that is named **Sales group line picking – User directed**.</span></span>
2. <span data-ttu-id="0fb53-109">Under **Mobilenhedsmenupunkt** angives følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="0fb53-109">Under **Mobile device menu items**, set the following values:</span></span>

    - <span data-ttu-id="0fb53-110">I feltet **Navn for menupunkt** indtastes **Salgspluk - gruppelinje**.</span><span class="sxs-lookup"><span data-stu-id="0fb53-110">In the **Menu item name** field, enter **Sales Pick - Group line**.</span></span>
    - <span data-ttu-id="0fb53-111">I feltet **Titel** indtastes **Salgspluk - gruppelinje**.</span><span class="sxs-lookup"><span data-stu-id="0fb53-111">In the **Title** field, enter **Sales Pick - Group line**.</span></span>
    - <span data-ttu-id="0fb53-112">Vælg **Arbejde** i feltet **Tilstand**.</span><span class="sxs-lookup"><span data-stu-id="0fb53-112">In the **Mode** field, select **Work**.</span></span>
    - <span data-ttu-id="0fb53-113">Angiv indstillingen **Brug eksisterende arbejde** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="0fb53-113">Set the **Use existing work** option to **Yes**.</span></span>

3. <span data-ttu-id="0fb53-114">I oversigtspanelet **Generelt** kan du angive følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="0fb53-114">On the **General** FastTab, you can set the following values:</span></span>

    - <span data-ttu-id="0fb53-115">I feltet **Styret af** skal du vælge **Brugerstyret**.</span><span class="sxs-lookup"><span data-stu-id="0fb53-115">In the **Directed by** field, select **User directed**.</span></span>
    - <span data-ttu-id="0fb53-116">Angiv indstillingen **Generer nummerplade** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="0fb53-116">Set the **Generate license plate** option to **Yes**.</span></span>
    - <span data-ttu-id="0fb53-117">Angiv indstillingen **Gruppepluk** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="0fb53-117">Set the **Group pick** option to **Yes**.</span></span>

4. <span data-ttu-id="0fb53-118">I oversigtspanelet **Arbejdsklasser** skal du følge disse trin for at konfigurere de gyldige arbejdsklasser for menupunktet mobilenhed:</span><span class="sxs-lookup"><span data-stu-id="0fb53-118">On the **Work classes** FastTab, follow these steps to configure the valid work classes for the mobile device menu item:</span></span>

    1. <span data-ttu-id="0fb53-119">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="0fb53-119">Select **New**.</span></span>
    2. <span data-ttu-id="0fb53-120">I feltet **Arbejdsklasse-ID** skal du vælge **Salg** eller **SO pluk**, afhængigt af det lagersted, du vil bruge.</span><span class="sxs-lookup"><span data-stu-id="0fb53-120">In the **Work class ID** field, select **Sales** or **SO Pick**, depending on the warehouse that you will use.</span></span>
    3. <span data-ttu-id="0fb53-121">I feltet **Arbejdsordretype** skal du vælge **Salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="0fb53-121">In the **Work order type** field, select **Sales orders**.</span></span>

### <a name="set-up-a-mobile-device-menu"></a><span data-ttu-id="0fb53-122">Opsætning af en mobilenhedsmenu</span><span class="sxs-lookup"><span data-stu-id="0fb53-122">Set up a mobile device menu</span></span>

1. <span data-ttu-id="0fb53-123">Gå til **Lagerstedsstyring \> Opsætning \> Mobilenhed \> Mobilenhedsmenu**.</span><span class="sxs-lookup"><span data-stu-id="0fb53-123">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span> 
1. <span data-ttu-id="0fb53-124">Tilføj det menupunkt, du lige har oprettet, til den ønskede menu.</span><span class="sxs-lookup"><span data-stu-id="0fb53-124">Add the menu item that you just created to the desired menu.</span></span>

### <a name="set-up-a-work-template"></a><span data-ttu-id="0fb53-125">Opsætning af en arbejdsskabelon</span><span class="sxs-lookup"><span data-stu-id="0fb53-125">Set up a work template</span></span>

1. <span data-ttu-id="0fb53-126">Gå til **Lagerstedsstyring \> Opsætning \> Arbejde \> Arbejdsskabeloner**.</span><span class="sxs-lookup"><span data-stu-id="0fb53-126">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="0fb53-127">Find den arbejdsskabelon, der skal bruges med denne funktion.</span><span class="sxs-lookup"><span data-stu-id="0fb53-127">Find the work template that should be used with this function.</span></span> <span data-ttu-id="0fb53-128">I dette eksempel skal du vælge Contoso-standardarbejdsskabelonen **51 pluk til stadie**.</span><span class="sxs-lookup"><span data-stu-id="0fb53-128">For this example, select the standard **51 Pick to stage** Contoso work template.</span></span>
1. <span data-ttu-id="0fb53-129">Vælg **Rediger forespørgsel** i menuen.</span><span class="sxs-lookup"><span data-stu-id="0fb53-129">On the menu, select **Edit query**.</span></span>
1. <span data-ttu-id="0fb53-130">Under fanen **Sortering** skal du vælge **Tilføj** og derefter angive følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="0fb53-130">On the **Sorting** tab, select **Add**, and then set the following values:</span></span>

    - <span data-ttu-id="0fb53-131">Vælg **Midlertidige arbejdstransaktioner** i feltet **Tabel**.</span><span class="sxs-lookup"><span data-stu-id="0fb53-131">In the **Table** field, select **Temporary work transactions**.</span></span>
    - <span data-ttu-id="0fb53-132">Vælg **Midlertidige arbejdstransaktioner** i feltet **Afledt tabel**.</span><span class="sxs-lookup"><span data-stu-id="0fb53-132">In the **Derived table** field, select **Temporary work transactions**.</span></span>
    - <span data-ttu-id="0fb53-133">I feltet **Felt** skal du vælge **Varenummer**.</span><span class="sxs-lookup"><span data-stu-id="0fb53-133">In the **Field** field, select **Item number**.</span></span>
    - <span data-ttu-id="0fb53-134">I feltet **Søgeretning** skal du vælge **Stigende**.</span><span class="sxs-lookup"><span data-stu-id="0fb53-134">In the **Search direction** field, select **Ascending**.</span></span>

> [!NOTE]
> <span data-ttu-id="0fb53-135">Hvis funktionen pluklinjegruppering skal fungere, skal arbejdslinjerne sorteres efter vare-ID.</span><span class="sxs-lookup"><span data-stu-id="0fb53-135">For the pick line grouping functionality to work, the work lines must be sorted by item ID.</span></span> <span data-ttu-id="0fb53-136">Hvis de linjer, der har de samme elementer, ikke sorteres en efter en, grupperes de ikke.</span><span class="sxs-lookup"><span data-stu-id="0fb53-136">If lines that have the same items aren't sequenced one after another, they won't be grouped.</span></span>

## <a name="example"></a><span data-ttu-id="0fb53-137">Eksempel</span><span class="sxs-lookup"><span data-stu-id="0fb53-137">Example</span></span>

### <a name="create-picking-work"></a><span data-ttu-id="0fb53-138">Opret plukarbejde</span><span class="sxs-lookup"><span data-stu-id="0fb53-138">Create picking work</span></span>

<span data-ttu-id="0fb53-139">Før du kan konfigurere pluklinjegruppering, skal du oprette noget kvalificeret udgående arbejde.</span><span class="sxs-lookup"><span data-stu-id="0fb53-139">Before you can set up pick line grouping, you must create some eligible outbound work.</span></span>

1. <span data-ttu-id="0fb53-140">Gå til **Sales and MArketing \> Salgsordrer \> Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="0fb53-140">Go to **Sales and Marketing \> Sales orders \> All sales orders**.</span></span>
2. <span data-ttu-id="0fb53-141">Vælg **Ny** for at oprette en ny salgsordre.</span><span class="sxs-lookup"><span data-stu-id="0fb53-141">Select **New** to create a sales order.</span></span> 
3. <span data-ttu-id="0fb53-142">Vælg en kunde i feltet **Kundekonto**.</span><span class="sxs-lookup"><span data-stu-id="0fb53-142">In the **Customer account** field, select any customer.</span></span> 
4. <span data-ttu-id="0fb53-143">I oversigtspanelet **Generelt** skal du i feltet **Lagersted** vælge **51**.</span><span class="sxs-lookup"><span data-stu-id="0fb53-143">On the **General** FastTab, in the **Warehouse** field, select **51**.</span></span> <span data-ttu-id="0fb53-144">Vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="0fb53-144">Then select **OK**.</span></span>
5. <span data-ttu-id="0fb53-145">Tilføj følgende seks linjer under **Salgsordrelinjer**:</span><span class="sxs-lookup"><span data-stu-id="0fb53-145">Under **Sales order lines**, add the following six lines:</span></span>

    - <span data-ttu-id="0fb53-146">**Linje 1:** I feltet **Varenummer** skal du vælge **M9200**.</span><span class="sxs-lookup"><span data-stu-id="0fb53-146">**Line 1:** In the **Item number** field, select **M9200**.</span></span> <span data-ttu-id="0fb53-147">Angiv **3** i feltet **Antal**.</span><span class="sxs-lookup"><span data-stu-id="0fb53-147">In the **Quantity** field, enter **3**.</span></span>
    - <span data-ttu-id="0fb53-148">**Linje 2:** I feltet **Varenummer** skal du vælge **M9201**.</span><span class="sxs-lookup"><span data-stu-id="0fb53-148">**Line 2:** In the **Item number** field, select **M9201**.</span></span> <span data-ttu-id="0fb53-149">Angiv **3** i feltet **Antal**.</span><span class="sxs-lookup"><span data-stu-id="0fb53-149">In the **Quantity** field, enter **3**.</span></span> 
    - <span data-ttu-id="0fb53-150">**Linje 3:** I feltet **Varenummer** skal du vælge **M9202**.</span><span class="sxs-lookup"><span data-stu-id="0fb53-150">**Line 3:** In the **Item number** field, select **M9202**.</span></span> <span data-ttu-id="0fb53-151">Angiv **2** i feltet **Antal**.</span><span class="sxs-lookup"><span data-stu-id="0fb53-151">In the **Quantity** field, enter **2**.</span></span> 
    - <span data-ttu-id="0fb53-152">**Linje 4:** I feltet **Varenummer** skal du vælge **M9200**.</span><span class="sxs-lookup"><span data-stu-id="0fb53-152">**Line 4:** In the **Item number** field, select **M9200**.</span></span> <span data-ttu-id="0fb53-153">Angiv **1** i feltet **Antal**.</span><span class="sxs-lookup"><span data-stu-id="0fb53-153">In the **Quantity** field, enter **1**.</span></span> 
    - <span data-ttu-id="0fb53-154">**Linje 5:** I feltet **Varenummer** skal du vælge **M9200**.</span><span class="sxs-lookup"><span data-stu-id="0fb53-154">**Line 5:** In the **Item number** field, select **M9200**.</span></span> <span data-ttu-id="0fb53-155">Angiv **3** i feltet **Antal**.</span><span class="sxs-lookup"><span data-stu-id="0fb53-155">In the **Quantity** field, enter **3**.</span></span>
    - <span data-ttu-id="0fb53-156">**Linje 6:** I feltet **Varenummer** skal du vælge **M9202**.</span><span class="sxs-lookup"><span data-stu-id="0fb53-156">**Line 6:** In the **Item number** field, select **M9202**.</span></span> <span data-ttu-id="0fb53-157">Angiv **7** i feltet **Antal**.</span><span class="sxs-lookup"><span data-stu-id="0fb53-157">In the **Quantity** field, enter **7**.</span></span> 

    <span data-ttu-id="0fb53-158">Her er en oversigt over de samlede mængder af hver vare:</span><span class="sxs-lookup"><span data-stu-id="0fb53-158">Here is a summary of the total quantities for each item:</span></span>

    - <span data-ttu-id="0fb53-159">**Vare M9200:** 7 hver</span><span class="sxs-lookup"><span data-stu-id="0fb53-159">**Item M9200:** 7 each</span></span>
    - <span data-ttu-id="0fb53-160">**Vare M9201:** 3 hver</span><span class="sxs-lookup"><span data-stu-id="0fb53-160">**Item M9201:** 3 each</span></span>
    - <span data-ttu-id="0fb53-161">**Vare M9202:** 9 hver</span><span class="sxs-lookup"><span data-stu-id="0fb53-161">**Item M9202:** 9 each</span></span>

6. <span data-ttu-id="0fb53-162">Før du frigiver ordrerne til lageret, skal du sørge for, at plukstederne har tilstrækkelig lagerbeholdning af alle varerne på alle ordrerne.</span><span class="sxs-lookup"><span data-stu-id="0fb53-162">Before you release the orders to the warehouse, you must make sure that the pick locations have enough inventory for all the items on all the orders.</span></span> <span data-ttu-id="0fb53-163">Gennemse indstillingen **Lokationsvejledning** for at bestemme, hvilke pluksteder der skal bruges til salgsordrepluk.</span><span class="sxs-lookup"><span data-stu-id="0fb53-163">Review the **Location directive** setting to determine which picking locations are used for sales order picking.</span></span>
7. <span data-ttu-id="0fb53-164">Reserver lageret, og frigør det til lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="0fb53-164">Reserve the inventory, and release it to the warehouse.</span></span> <span data-ttu-id="0fb53-165">Der oprettes et arbejds-ID med seks linjer.</span><span class="sxs-lookup"><span data-stu-id="0fb53-165">A work ID that has six lines is created.</span></span> <span data-ttu-id="0fb53-166">Linjerne sorteres efter varenummer.</span><span class="sxs-lookup"><span data-stu-id="0fb53-166">The lines are sorted by item number.</span></span>

### <a name="run-the-mobile-device-flow"></a><span data-ttu-id="0fb53-167">Kør mobilenhedsprocessen</span><span class="sxs-lookup"><span data-stu-id="0fb53-167">Run the mobile device flow</span></span>

1. <span data-ttu-id="0fb53-168">På mobilenheden skal du vælge den menu, der indeholder det nye mobilenhedsmenupunkt.</span><span class="sxs-lookup"><span data-stu-id="0fb53-168">On the mobile device, select the menu that includes the new mobile device menu item.</span></span>
1. <span data-ttu-id="0fb53-169">Vælg menupunktet **Salgspluk – gruppelinje**, og påbegynd plukningen.</span><span class="sxs-lookup"><span data-stu-id="0fb53-169">Select the **Sales Pick – Group line** menu item, and initiate the pick.</span></span>

    <span data-ttu-id="0fb53-170">Når du har valgt menuen og indtastet arbejds-ID'et, får du vist trinnet pluk, hvor alle pluklinjer for vare M9200 grupperes.</span><span class="sxs-lookup"><span data-stu-id="0fb53-170">After you select the menu and enter the work ID, you see the pick step where all pick lines for item M9200 are grouped.</span></span> <span data-ttu-id="0fb53-171">Du modtager en instruktion om at plukke 7 hver af vare M9200.</span><span class="sxs-lookup"><span data-stu-id="0fb53-171">You receive an instruction to pick 7 each of item M9200.</span></span>

1. <span data-ttu-id="0fb53-172">Bekræft plukningstrinnet.</span><span class="sxs-lookup"><span data-stu-id="0fb53-172">Confirm the pick step.</span></span> 
1. <span data-ttu-id="0fb53-173">Gå til klientens skærm for det igangværende arbejde, og læg mærke til, at alle tre pluklinjer for vare M9200 blev lukket samtidigt.</span><span class="sxs-lookup"><span data-stu-id="0fb53-173">Go to the client screen of the work in process, and notice that all three pick lines for item M9200 were closed simultaneously.</span></span>

    <span data-ttu-id="0fb53-174">Arbejdslinje 4 præsenteres.</span><span class="sxs-lookup"><span data-stu-id="0fb53-174">Work line 4 is presented.</span></span>

1. <span data-ttu-id="0fb53-175">Bekræft plukningstrinnet.</span><span class="sxs-lookup"><span data-stu-id="0fb53-175">Confirm the pick step.</span></span>

    <span data-ttu-id="0fb53-176">Det sidste plukningstrin på mobilenheden aggregerer de sidste to pluklinjer fra arbejdsordren.</span><span class="sxs-lookup"><span data-stu-id="0fb53-176">The last pick step on the mobile device aggregates the last two pick lines from the work order.</span></span>

1. <span data-ttu-id="0fb53-177">Fuldfør pluktrinnet for 9 hver af vare M9202.</span><span class="sxs-lookup"><span data-stu-id="0fb53-177">Complete the pick step for 9 each of item M9202.</span></span>
1. <span data-ttu-id="0fb53-178">Bekræft læg på lager-trinnet og eventuelle ekstra pluk-/læg på lager-par for at fuldføre arbejdet.</span><span class="sxs-lookup"><span data-stu-id="0fb53-178">Confirm the put step and any additional pick/put pairs to complete the work.</span></span>

> [!NOTE]
> - <span data-ttu-id="0fb53-179">Arbejdslinjer kan kun grupperes, hvis de er i rækkefølge.</span><span class="sxs-lookup"><span data-stu-id="0fb53-179">Work lines can be grouped only if they are in sequence.</span></span>
> - <span data-ttu-id="0fb53-180">Følgende funktionalitet understøttes ikke:</span><span class="sxs-lookup"><span data-stu-id="0fb53-180">The following functionality isn't supported:</span></span>
>
>    - <span data-ttu-id="0fb53-181">Fastvægtvarer.</span><span class="sxs-lookup"><span data-stu-id="0fb53-181">Catch-weight items.</span></span> <span data-ttu-id="0fb53-182">Hvis der er nogen fastvægtvarer på arbejdet, får du vist en fejlmeddelelse, før du begynder at plukke.</span><span class="sxs-lookup"><span data-stu-id="0fb53-182">If there are any catch-weight items on the work, you receive an error message before you start to pick.</span></span>
>    - <span data-ttu-id="0fb53-183">Stykplukning</span><span class="sxs-lookup"><span data-stu-id="0fb53-183">Piece picking.</span></span>
>    - <span data-ttu-id="0fb53-184">Arbejdslinjer, der har uafsluttede genopfyldningsarbejde.</span><span class="sxs-lookup"><span data-stu-id="0fb53-184">Work lines that have unfinished replenishment work.</span></span>
>    - <span data-ttu-id="0fb53-185">Overplukning.</span><span class="sxs-lookup"><span data-stu-id="0fb53-185">Over-picking.</span></span>
