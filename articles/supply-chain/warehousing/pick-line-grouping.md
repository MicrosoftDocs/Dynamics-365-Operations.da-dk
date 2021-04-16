---
title: Pluklinjegruppering
description: Dette emne indeholder en oversigt over pluklinjegruppering.
author: Mirzaab
ms.date: 12/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFMenuItem,WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: fe0e63ef742b7bfd09684a94d273a1841d24599c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828267"
---
# <a name="pick-line-grouping"></a><span data-ttu-id="d6af3-103">Pluklinjegruppering</span><span class="sxs-lookup"><span data-stu-id="d6af3-103">Pick line grouping</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d6af3-104">Med pluklinjegruppering kan flere arbejdslinjer, der har samme vare og lokation, kombineres til et enkelt pluk, der præsenteres for brugeren på mobilenheden.</span><span class="sxs-lookup"><span data-stu-id="d6af3-104">Pick line grouping enables multiple work lines that have the same item and location to be combined into a single pick that is presented to the user on the mobile device.</span></span> <span data-ttu-id="d6af3-105">Derfor kan lagermedarbejderne modtage de mest mulige effektive instruktioner, men den påkrævede adskillelse af linjer (f.eks. for forskellige containere og ordrer) kan stadig bibeholdes i systemet.</span><span class="sxs-lookup"><span data-stu-id="d6af3-105">Therefore, warehouse workers can receive the most efficient instructions, but required work line separation (for different containers, orders, and so on) can still be maintained in the system.</span></span>

## <a name="turn-on-the-pick-line-grouping-feature"></a><span data-ttu-id="d6af3-106">Aktivere funktionen pluklinjegruppering</span><span class="sxs-lookup"><span data-stu-id="d6af3-106">Turn on the pick line grouping feature</span></span>

<span data-ttu-id="d6af3-107">Før du kan bruge denne funktion, skal den være slået til i dit system.</span><span class="sxs-lookup"><span data-stu-id="d6af3-107">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="d6af3-108">Administratorer kan bruge arbejdsområdet [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til efter behov.</span><span class="sxs-lookup"><span data-stu-id="d6af3-108">Administrators can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="d6af3-109">Dér vises funktionen på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="d6af3-109">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="d6af3-110">**Modul:** *Lokationsstyring*</span><span class="sxs-lookup"><span data-stu-id="d6af3-110">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="d6af3-111">**Funktionsnavn:** *Pluklinjegruppering*</span><span class="sxs-lookup"><span data-stu-id="d6af3-111">**Feature name:** *Pick line grouping*</span></span>

## <a name="set-up-pick-line-grouping"></a><span data-ttu-id="d6af3-112">Opsætning af pluklinjegruppering</span><span class="sxs-lookup"><span data-stu-id="d6af3-112">Set up pick line grouping</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="d6af3-113">Oprette et menupunkt på en mobilenhed</span><span class="sxs-lookup"><span data-stu-id="d6af3-113">Create a mobile device menu item</span></span>

1. <span data-ttu-id="d6af3-114">Gå til **Lagerstedsstyring \> Opsætning \> Mobilenhed \> Menupunkter i mobilenhed**.</span><span class="sxs-lookup"><span data-stu-id="d6af3-114">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="d6af3-115">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="d6af3-115">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="d6af3-116">I feltet **Navn for menupunkt** indtastes *Salgsgruppelinjeplukning*.</span><span class="sxs-lookup"><span data-stu-id="d6af3-116">In the **Menu item name** field, enter *Sales group line picking*.</span></span>
1. <span data-ttu-id="d6af3-117">I feltet **Titel** indtastes *Salgsgruppelinjeplukning*.</span><span class="sxs-lookup"><span data-stu-id="d6af3-117">In the **Title** field, enter *Sales group line picking*.</span></span> <span data-ttu-id="d6af3-118">Denne titel vises i menuen på mobilenheden.</span><span class="sxs-lookup"><span data-stu-id="d6af3-118">This title will be shown on the mobile device menu.</span></span>
1. <span data-ttu-id="d6af3-119">Vælg **Arbejde** i feltet *Tilstand*.</span><span class="sxs-lookup"><span data-stu-id="d6af3-119">In the **Mode** field, select *Work*.</span></span>
1. <span data-ttu-id="d6af3-120">Angiv indstillingen **Brug eksisterende arbejde** til *Ja*.</span><span class="sxs-lookup"><span data-stu-id="d6af3-120">Set the **Use existing work** option to *Yes*.</span></span>
1. <span data-ttu-id="d6af3-121">I oversigtspanelet **Generelt** kan du angive følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="d6af3-121">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="d6af3-122">I feltet **Styret af** skal du vælge *Brugerstyret*.</span><span class="sxs-lookup"><span data-stu-id="d6af3-122">In the **Directed by** field, select *User directed*.</span></span>
    - <span data-ttu-id="d6af3-123">Angiv indstillingen **Generer nummerplade** til *Ja*.</span><span class="sxs-lookup"><span data-stu-id="d6af3-123">Set the **Generate license plate** option to *Yes*.</span></span>
    - <span data-ttu-id="d6af3-124">Angiv indstillingen **Gruppepluk** til *Ja*.</span><span class="sxs-lookup"><span data-stu-id="d6af3-124">Set the **Group pick** option to *Yes*.</span></span>
    - <span data-ttu-id="d6af3-125">Acceptér standardværdierne for alle de andre indstillinger.</span><span class="sxs-lookup"><span data-stu-id="d6af3-125">Accept the default values for the remaining options.</span></span>

1. <span data-ttu-id="d6af3-126">Følg disse trin for at konfigurere de gyldige arbejdsklasser for menupunktet mobilenhed:</span><span class="sxs-lookup"><span data-stu-id="d6af3-126">Follow these steps to configure the valid work classes for the mobile device menu item:</span></span>

    1. <span data-ttu-id="d6af3-127">I oversigtspanelet **Arbejdsklasser** skal du vælge **Ny**.</span><span class="sxs-lookup"><span data-stu-id="d6af3-127">On the **Work classes** FastTab, elect **New**.</span></span>
    2. <span data-ttu-id="d6af3-128">I feltet **Arbejdsklasse-id** skal du vælge enten *Salg* eller *Salgsordrepluk*, afhængigt af det lagersted, du vil bruge.</span><span class="sxs-lookup"><span data-stu-id="d6af3-128">In the **Work class ID** field, you can select either *Sales* or *SO Pick*, depending on the warehouse that you will use.</span></span> <span data-ttu-id="d6af3-129">Vælg *Salgsordrepluk* for dette scenario.</span><span class="sxs-lookup"><span data-stu-id="d6af3-129">For this scenario, select *SO Pick*.</span></span>

        <span data-ttu-id="d6af3-130">Feltet **Arbejdsordretype** er automatisk angivet til *Salgsordrer*.</span><span class="sxs-lookup"><span data-stu-id="d6af3-130">The **Work order type** field is automatically set to *Sales orders*.</span></span>

### <a name="set-up-a-mobile-device-menu"></a><span data-ttu-id="d6af3-131">Opsætning af en mobilenhedsmenu</span><span class="sxs-lookup"><span data-stu-id="d6af3-131">Set up a mobile device menu</span></span>

<span data-ttu-id="d6af3-132">Følg disse trin for at føje det menupunkt, du lige har oprettet, til menuen **Udgående**.</span><span class="sxs-lookup"><span data-stu-id="d6af3-132">Follow these steps to add the menu item that you just created to the **Outbound** menu.</span></span>

1. <span data-ttu-id="d6af3-133">Gå til **Lagerstedsstyring \> Opsætning \> Mobilenhed \> Mobilenhedsmenu**.</span><span class="sxs-lookup"><span data-stu-id="d6af3-133">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="d6af3-134">Vælg **Rediger** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="d6af3-134">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="d6af3-135">I listeruden vises alle eksisterende menuer for mobilenheder.</span><span class="sxs-lookup"><span data-stu-id="d6af3-135">The list pane shows all existing mobile device menus.</span></span> <span data-ttu-id="d6af3-136">Vælg *Udgående* på listen.</span><span class="sxs-lookup"><span data-stu-id="d6af3-136">Select *Outbound* in the list.</span></span>
1. <span data-ttu-id="d6af3-137">På listen **Tilgængelige menuer og menupunkter** skal du finde og vælge menupunktet *Salgsgruppelinjeplukning*, du har oprettet.</span><span class="sxs-lookup"><span data-stu-id="d6af3-137">In the **Available menus and menu items** list, find and select the *Sales group line picking* menu item that you created.</span></span>
1. <span data-ttu-id="d6af3-138">Vælg den højre pileknap for at flytte menupunktet *Salgsgruppelinjeplukning* til listen **Menustruktur**.</span><span class="sxs-lookup"><span data-stu-id="d6af3-138">Select the right arrow button to move the *Sales group line picking* menu item to the **Menu structure** list.</span></span>
1. <span data-ttu-id="d6af3-139">Brug knapperne Pil op og Pil ned til at flytte menupunktet til den ønskede placering i menustrukturen.</span><span class="sxs-lookup"><span data-stu-id="d6af3-139">Use the up arrow and down arrow buttons to move the menu item into the desired position in the menu structure.</span></span>
1. <span data-ttu-id="d6af3-140">Vælg **Gem** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="d6af3-140">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-a-work-template"></a><span data-ttu-id="d6af3-141">Opsætning af en arbejdsskabelon</span><span class="sxs-lookup"><span data-stu-id="d6af3-141">Set up a work template</span></span>

1. <span data-ttu-id="d6af3-142">Gå til **Lagerstedsstyring \> Opsætning \> Arbejde \> Arbejdsskabeloner**.</span><span class="sxs-lookup"><span data-stu-id="d6af3-142">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="d6af3-143">I feltet **Arbejdsordretype** skal du vælge *Salgsordrer*.</span><span class="sxs-lookup"><span data-stu-id="d6af3-143">In the **Work order type** field, select *Sales orders*.</span></span>
1. <span data-ttu-id="d6af3-144">Find og vælg den arbejdsskabelon, der skal bruges sammen med denne funktion, i gitteret **Oversigt**.</span><span class="sxs-lookup"><span data-stu-id="d6af3-144">In the **Overview** grid, find and select the work template that should be used with this function.</span></span> <span data-ttu-id="d6af3-145">I dette scenario skal du vælge skabelonen *51 Pluk til midlertidigt lager*.</span><span class="sxs-lookup"><span data-stu-id="d6af3-145">For this scenario, select the *51 Pick to stage* template.</span></span>
1. <span data-ttu-id="d6af3-146">Vælg **Rediger forespørgsel** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="d6af3-146">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="d6af3-147">I dialogboksen for forespørgselseditoren skal du på fanen **Sortering** vælge **Tilføj** og derefter indstille følgende værdier for den nye række:</span><span class="sxs-lookup"><span data-stu-id="d6af3-147">In the query editor dialog box, on the **Sorting** tab, select **Add**, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="d6af3-148">Vælg *Midlertidige arbejdstransaktioner* i kolonnen **Tabel**.</span><span class="sxs-lookup"><span data-stu-id="d6af3-148">In the **Table** column, select *Temporary work transactions*.</span></span>
    - <span data-ttu-id="d6af3-149">Vælg *Midlertidige arbejdstransaktioner* i kolonnen **Afledt tabel**.</span><span class="sxs-lookup"><span data-stu-id="d6af3-149">In the **Derived table** column, select *Temporary work transactions*.</span></span>
    - <span data-ttu-id="d6af3-150">I kolonnen **Felt** skal du vælge *Varenummer*.</span><span class="sxs-lookup"><span data-stu-id="d6af3-150">In the **Field** column, select *Item number*.</span></span>
    - <span data-ttu-id="d6af3-151">I kolonnen **Søgeretning** skal du vælge *Stigende*.</span><span class="sxs-lookup"><span data-stu-id="d6af3-151">In the **Search direction** column, select *Ascending*.</span></span>

1. <span data-ttu-id="d6af3-152">Vælg **OK** for at lukke dialogboksen gemme dine valg.</span><span class="sxs-lookup"><span data-stu-id="d6af3-152">Select **OK** to close the dialog box and save your selection.</span></span>
1. <span data-ttu-id="d6af3-153">Du får vist følgende meddelelse: "Gruppering vil blive nulstillet, vil du fortsætte?"</span><span class="sxs-lookup"><span data-stu-id="d6af3-153">You receive the following message: "Grouping will be reset, continue?"</span></span> <span data-ttu-id="d6af3-154">Vælg **Ja** for at fortsætte.</span><span class="sxs-lookup"><span data-stu-id="d6af3-154">Select **Yes** to continue.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d6af3-155">Hvis funktionen pluklinjegruppering skal fungere, skal arbejdslinjerne sorteres efter vare-ID.</span><span class="sxs-lookup"><span data-stu-id="d6af3-155">For the pick line grouping functionality to work, the work lines must be sorted by item ID.</span></span> <span data-ttu-id="d6af3-156">Hvis de linjer, der har de samme elementer, ikke sorteres en efter en, grupperes de ikke.</span><span class="sxs-lookup"><span data-stu-id="d6af3-156">If lines that have the same items aren't sequenced one after another, they won't be grouped.</span></span>

## <a name="example"></a><span data-ttu-id="d6af3-157">Eksempel</span><span class="sxs-lookup"><span data-stu-id="d6af3-157">Example</span></span>

### <a name="create-picking-work"></a><span data-ttu-id="d6af3-158">Opret plukarbejde</span><span class="sxs-lookup"><span data-stu-id="d6af3-158">Create picking work</span></span>

<span data-ttu-id="d6af3-159">Før du kan konfigurere pluklinjegruppering, skal du oprette noget kvalificeret udgående arbejde.</span><span class="sxs-lookup"><span data-stu-id="d6af3-159">Before you can set up pick line grouping, you must create some eligible outbound work.</span></span>

1. <span data-ttu-id="d6af3-160">Gå til **Salg og marketing \> Salgsordrer \> Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="d6af3-160">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="d6af3-161">Vælg **Ny** for at oprette en ny salgsordre.</span><span class="sxs-lookup"><span data-stu-id="d6af3-161">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="d6af3-162">Vælg **US-004** i feltet *Debitorkonto*.</span><span class="sxs-lookup"><span data-stu-id="d6af3-162">In the **Customer account** field, select *US-004*.</span></span>
1. <span data-ttu-id="d6af3-163">I oversigtspanelet **Generelt** skal du i feltet **Lagersted** vælge *51*.</span><span class="sxs-lookup"><span data-stu-id="d6af3-163">On the **General** FastTab, in the **Warehouse** field, select *51*.</span></span>
1. <span data-ttu-id="d6af3-164">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="d6af3-164">Select **OK**.</span></span>
1. <span data-ttu-id="d6af3-165">Tilføj følgende seks linjer på oversigtspanelet **Salgsordrelinjer**:</span><span class="sxs-lookup"><span data-stu-id="d6af3-165">On the **Sales order lines** FastTab, add the following six lines:</span></span>

    - <span data-ttu-id="d6af3-166">**Linje 1:** I feltet **Varenummer** skal du vælge *M9200*.</span><span class="sxs-lookup"><span data-stu-id="d6af3-166">**Line 1:** In the **Item number** field, select *M9200*.</span></span> <span data-ttu-id="d6af3-167">Angiv **3** i feltet *Antal*.</span><span class="sxs-lookup"><span data-stu-id="d6af3-167">In the **Quantity** field, enter *3*.</span></span>
    - <span data-ttu-id="d6af3-168">**Linje 2:** I feltet **Varenummer** skal du vælge *M9201*.</span><span class="sxs-lookup"><span data-stu-id="d6af3-168">**Line 2:** In the **Item number** field, select *M9201*.</span></span> <span data-ttu-id="d6af3-169">Angiv **3** i feltet *Antal*.</span><span class="sxs-lookup"><span data-stu-id="d6af3-169">In the **Quantity** field, enter *3*.</span></span>
    - <span data-ttu-id="d6af3-170">**Linje 3:** I feltet **Varenummer** skal du vælge *M9202*.</span><span class="sxs-lookup"><span data-stu-id="d6af3-170">**Line 3:** In the **Item number** field, select *M9202*.</span></span> <span data-ttu-id="d6af3-171">Angiv **2** i feltet *Antal*.</span><span class="sxs-lookup"><span data-stu-id="d6af3-171">In the **Quantity** field, enter *2*.</span></span>
    - <span data-ttu-id="d6af3-172">**Linje 4:** I feltet **Varenummer** skal du vælge *M9200*.</span><span class="sxs-lookup"><span data-stu-id="d6af3-172">**Line 4:** In the **Item number** field, select *M9200*.</span></span> <span data-ttu-id="d6af3-173">Angiv **1** i feltet *Antal*.</span><span class="sxs-lookup"><span data-stu-id="d6af3-173">In the **Quantity** field, enter *1*.</span></span>
    - <span data-ttu-id="d6af3-174">**Linje 5:** I feltet **Varenummer** skal du vælge *M9200*.</span><span class="sxs-lookup"><span data-stu-id="d6af3-174">**Line 5:** In the **Item number** field, select *M9200*.</span></span> <span data-ttu-id="d6af3-175">Angiv **3** i feltet *Antal*.</span><span class="sxs-lookup"><span data-stu-id="d6af3-175">In the **Quantity** field, enter *3*.</span></span>
    - <span data-ttu-id="d6af3-176">**Linje 6:** I feltet **Varenummer** skal du vælge *M9202*.</span><span class="sxs-lookup"><span data-stu-id="d6af3-176">**Line 6:** In the **Item number** field, select *M9202*.</span></span> <span data-ttu-id="d6af3-177">Angiv **7** i feltet *Antal*.</span><span class="sxs-lookup"><span data-stu-id="d6af3-177">In the **Quantity** field, enter *7*.</span></span>

    <span data-ttu-id="d6af3-178">Her er en oversigt over de samlede mængder af hver vare:</span><span class="sxs-lookup"><span data-stu-id="d6af3-178">Here is a summary of the total quantities for each item:</span></span>

    - <span data-ttu-id="d6af3-179">**Vare M9200:** *7* hver</span><span class="sxs-lookup"><span data-stu-id="d6af3-179">**Item M9200:** *7* each</span></span>
    - <span data-ttu-id="d6af3-180">**Vare M9201:** *3* hver</span><span class="sxs-lookup"><span data-stu-id="d6af3-180">**Item M9201:** *3* each</span></span>
    - <span data-ttu-id="d6af3-181">**Vare M9202:** *9* hver</span><span class="sxs-lookup"><span data-stu-id="d6af3-181">**Item M9202:** *9* each</span></span>

1. <span data-ttu-id="d6af3-182">Før du frigiver ordrerne til lageret, skal du sørge for, at plukstederne har tilstrækkelig lagerbeholdning af alle varerne på alle ordrerne.</span><span class="sxs-lookup"><span data-stu-id="d6af3-182">Before you release the orders to the warehouse, you must make sure that the pick locations have enough inventory for all the items on all the orders.</span></span> <span data-ttu-id="d6af3-183">Gennemse indstillingen **Lokationsvejledning** for at bestemme, hvilke pluksteder der skal bruges til salgsordrepluk.</span><span class="sxs-lookup"><span data-stu-id="d6af3-183">Review the **Location directive** setting to determine which picking locations are used for sales order picking.</span></span> <span data-ttu-id="d6af3-184">Hvis du bruger miljøet med demodata til Contoso for lagersted *51*, skal du bekræfte, at der er et tilgængeligt lager.</span><span class="sxs-lookup"><span data-stu-id="d6af3-184">If you're using the Contoso demo data environment for warehouse *51*, confirm that there is available inventory.</span></span>

    <span data-ttu-id="d6af3-185">Du skal nu reservere lageret for hver linje.</span><span class="sxs-lookup"><span data-stu-id="d6af3-185">You must now reserve the inventory for each line.</span></span>

1. <span data-ttu-id="d6af3-186">Vælg en af de linjer, der skal reserveres, på oversigtspanelet **Salgsordrelinjer**.</span><span class="sxs-lookup"><span data-stu-id="d6af3-186">On the **Sales order lines** FastTab, select one of the lines that must be reserved.</span></span>
1. <span data-ttu-id="d6af3-187">Vælg **reservation** i menuen **Lager** oven over gitteret.</span><span class="sxs-lookup"><span data-stu-id="d6af3-187">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="d6af3-188">På siden **Reservation** skal du i handlingsruden vælge **Reserver parti** for at anvende reservationen.</span><span class="sxs-lookup"><span data-stu-id="d6af3-188">On the **Reservation** page, on the Action Pane, select **Reserve lot** to apply the reservation.</span></span> <span data-ttu-id="d6af3-189">Luk derefter siden.</span><span class="sxs-lookup"><span data-stu-id="d6af3-189">Then close the page.</span></span>
1. <span data-ttu-id="d6af3-190">Gentag trin 8 til 10 for de øvrige linjer, der skal reserveres.</span><span class="sxs-lookup"><span data-stu-id="d6af3-190">Repeat steps 8 through 10 for the remaining lines that must be reserved.</span></span>

    <span data-ttu-id="d6af3-191">Du skal nu frigive salgsordren til lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="d6af3-191">You must now release the sales order to the warehouse.</span></span>

1. <span data-ttu-id="d6af3-192">Vælg **Frigør til lagersted** under fanen **Lagersted** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="d6af3-192">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="d6af3-193">Du modtager en meddelelse, der viser, at der er oprettet en forsendelse og en bølge, og at bølgen er sendt til kørsel i en batch.</span><span class="sxs-lookup"><span data-stu-id="d6af3-193">You receive a message that states that a shipment and a wave have been created, and that the wave has been submitted to run in a batch.</span></span>

    <span data-ttu-id="d6af3-194">Når bølgen og alle downstreamjob er fuldført, oprettes der et arbejds-id for arbejde med seks linjer.</span><span class="sxs-lookup"><span data-stu-id="d6af3-194">When the wave and all downstream jobs have been completed, a work ID is created for work that has six lines.</span></span> <span data-ttu-id="d6af3-195">Linjerne sorteres efter varenummer.</span><span class="sxs-lookup"><span data-stu-id="d6af3-195">The lines are sorted by item number.</span></span>

1. <span data-ttu-id="d6af3-196">Gå til **Lokationsstyring \> Arbejde \> Alt arbejde** for at få vist det oprettede arbejde.</span><span class="sxs-lookup"><span data-stu-id="d6af3-196">Go to **Warehouse management \> Work \> All work** to view the work that was created.</span></span> <span data-ttu-id="d6af3-197">Notér værdien i **Arbejds-id**, da du får brug for det i næste procedure.</span><span class="sxs-lookup"><span data-stu-id="d6af3-197">Make a note of the **Work ID** value, because you will need it in the next procedure.</span></span>

### <a name="initiate-picking-from-the-mobile-device"></a><span data-ttu-id="d6af3-198">Starte plukning fra mobilenheden</span><span class="sxs-lookup"><span data-stu-id="d6af3-198">Initiate picking from the mobile device</span></span>

1. <span data-ttu-id="d6af3-199">Log på mobilenheden som en bruger, der er konfigureret til lagersted *51*.</span><span class="sxs-lookup"><span data-stu-id="d6af3-199">Sign in to the mobile device as a user who is set up for warehouse *51*.</span></span>
1. <span data-ttu-id="d6af3-200">På mobilenheden skal du vælge den menu, der indeholder det nye mobilenhedsmenupunkt.</span><span class="sxs-lookup"><span data-stu-id="d6af3-200">On the mobile device, select the menu that includes the new mobile device menu item.</span></span> <span data-ttu-id="d6af3-201">Vælg **Udgående** for dette scenario.</span><span class="sxs-lookup"><span data-stu-id="d6af3-201">For this scenario, select **Outbound**.</span></span>
1. <span data-ttu-id="d6af3-202">Vælg menupunktet **Salgsgruppelinjeplukning** for at påbegynde plukningen.</span><span class="sxs-lookup"><span data-stu-id="d6af3-202">Select the **Sales group line picking** menu item to initiate the pick.</span></span>
1. <span data-ttu-id="d6af3-203">Angiv den værdi i **Arbejds-id**, som du noterede i den forrige procedure.</span><span class="sxs-lookup"><span data-stu-id="d6af3-203">Enter the **Work ID** value that you made a note of in the previous procedure.</span></span>

    <span data-ttu-id="d6af3-204">Du burde nu se et pluktrin, hvor alle pluklinjer for vare *M9200* er grupperet, og modtage en vejledning om at plukke *7* af hver vare *M9200*.</span><span class="sxs-lookup"><span data-stu-id="d6af3-204">You should see a pick step where all pick lines for item *M9200* are grouped, and you should receive an instruction to pick *7* each of item *M9200*.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="d6af3-205">På mobilenheden er plukarbejdet for de tre plukarbejdslinjer samlet i ét pluktrin for brugeren.</span><span class="sxs-lookup"><span data-stu-id="d6af3-205">On the mobile device, the pick work for the three pick work lines has been aggregated into one picking step for the user.</span></span>

1. <span data-ttu-id="d6af3-206">Bekræft plukningstrinnet.</span><span class="sxs-lookup"><span data-stu-id="d6af3-206">Confirm the pick step.</span></span>
1. <span data-ttu-id="d6af3-207">Gå til arbejdssiden for arbejds-id'et, og læg mærke til, at alle tre pluklinjer for vare *M9200* blev lukket samtidigt.</span><span class="sxs-lookup"><span data-stu-id="d6af3-207">Go to the work page for the work ID, and notice that all three pick lines for item *M9200* were closed simultaneously.</span></span>
1. <span data-ttu-id="d6af3-208">Gå tilbage til mobilenheden, og fortsæt med at plukke.</span><span class="sxs-lookup"><span data-stu-id="d6af3-208">Go back to the mobile device, and continue to pick.</span></span> <span data-ttu-id="d6af3-209">Arbejdslinje 4 for vare *M9201* burde vises.</span><span class="sxs-lookup"><span data-stu-id="d6af3-209">Work line 4 for item *M9201* should be presented.</span></span> <span data-ttu-id="d6af3-210">Da der kun var én arbejdslinje i ordren, er der intet, der skal samles.</span><span class="sxs-lookup"><span data-stu-id="d6af3-210">Because there was only one work line on the order, there is nothing to aggregate.</span></span>
1. <span data-ttu-id="d6af3-211">Bekræft plukningstrinnet.</span><span class="sxs-lookup"><span data-stu-id="d6af3-211">Confirm the pick step.</span></span>
1. <span data-ttu-id="d6af3-212">Det sidste plukningstrin på mobilenheden aggregerer de sidste to pluklinjer fra arbejdsordren.</span><span class="sxs-lookup"><span data-stu-id="d6af3-212">The last pick step on the mobile device aggregates the last two pick lines from the work order.</span></span>
1. <span data-ttu-id="d6af3-213">Fuldfør pluktrinnet for *9* hver af vare *M9202*.</span><span class="sxs-lookup"><span data-stu-id="d6af3-213">Complete the pick step for *9* each of item *M9202*.</span></span>
1. <span data-ttu-id="d6af3-214">Bekræft læg på lager-trinnet og eventuelle ekstra pluk-/læg på lager-par for at fuldføre arbejdet.</span><span class="sxs-lookup"><span data-stu-id="d6af3-214">Confirm the put step and any additional pick/put pairs to complete the work.</span></span>

> [!IMPORTANT]
>
> - <span data-ttu-id="d6af3-215">Arbejdslinjer kan kun grupperes, hvis de er i rækkefølge.</span><span class="sxs-lookup"><span data-stu-id="d6af3-215">Work lines can be grouped only if they are in sequence.</span></span>
> - <span data-ttu-id="d6af3-216">Følgende funktionalitet understøttes ikke:</span><span class="sxs-lookup"><span data-stu-id="d6af3-216">The following functionality isn't supported:</span></span>
>
>   - <span data-ttu-id="d6af3-217">Fastvægtvarer</span><span class="sxs-lookup"><span data-stu-id="d6af3-217">Catch-weight items</span></span>
>
>    <span data-ttu-id="d6af3-218">Hvis der er nogen fastvægtvarer på arbejdet, får du vist en fejlmeddelelse, før du begynder at plukke.</span><span class="sxs-lookup"><span data-stu-id="d6af3-218">If there are any catch-weight items on the work, you receive an error message before you start to pick.</span></span>
>
>   - <span data-ttu-id="d6af3-219">Stykplukning</span><span class="sxs-lookup"><span data-stu-id="d6af3-219">Piece picking</span></span>
>   - <span data-ttu-id="d6af3-220">Arbejdslinjer, der har uafsluttede genopfyldningsarbejde.</span><span class="sxs-lookup"><span data-stu-id="d6af3-220">Work lines that have unfinished replenishment work</span></span>
>   - <span data-ttu-id="d6af3-221">Overplukning</span><span class="sxs-lookup"><span data-stu-id="d6af3-221">Over-picking</span></span>
>   - <span data-ttu-id="d6af3-222">Kort plukning med vareomfordeling</span><span class="sxs-lookup"><span data-stu-id="d6af3-222">Short picking with item reallocation</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]