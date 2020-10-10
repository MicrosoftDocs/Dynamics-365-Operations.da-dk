---
title: Vedligeholdelsesprognoser
description: I dette emne beskrives vedligeholdelsesprognoser i Styring af aktiver.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderForecastToJournals, EntAssetWorkOrderForecast
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6428981fcf560c541634d9466695be7bce4cb453
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/25/2020
ms.locfileid: "3888947"
---
# <a name="maintenance-forecasts"></a><span data-ttu-id="cdba4-103">Vedligeholdelsesbudgetter</span><span class="sxs-lookup"><span data-stu-id="cdba4-103">Maintenance forecasts</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="cdba4-104">Når du opretter en arbejdsordre, opretter du arbejdsordrejob, der har relaterede aktiver og vedligeholdelsesjobtyper.</span><span class="sxs-lookup"><span data-stu-id="cdba4-104">When you create a work order, you create work order jobs that have related assets and maintenance job types.</span></span> <span data-ttu-id="cdba4-105">Når du vælger en vedligeholdelsesjobtype, der indeholder vedligeholdelsesprognoser, kopieres prognoserne automatisk til arbejdsordren.</span><span class="sxs-lookup"><span data-stu-id="cdba4-105">When you select a maintenance job type that contains maintenance forecasts, the forecasts are automatically copied to the work order.</span></span>

<span data-ttu-id="cdba4-106">Du kan muligvis føje prognoselinjer til en arbejdsordre eller slette dem fra en arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="cdba4-106">You might be able to add forecast lines to a work order or delete them from a work order.</span></span> <span data-ttu-id="cdba4-107">Opsætningen af en livscyklustilstand for en arbejdsordre, den relaterede projekttype og stadiereglerne, der er relateret til projekttypen, bestemmer, om du kan tilføje eller redigere prognoselinjer.</span><span class="sxs-lookup"><span data-stu-id="cdba4-107">The setup of the work order lifecycle state, the related project type, and the stage rules that are related to the project type determine whether you can add or edit forecast lines.</span></span> <span data-ttu-id="cdba4-108">Du kan finde flere oplysninger om arbejdsordrers livscyklustilstande og relaterede projektstadier i [Budgetter, arbejdsordrer og projekter](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span><span class="sxs-lookup"><span data-stu-id="cdba4-108">For more information about work order lifecycle states and related project stages, see [Forecasts, work orders, and projects](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span></span>

1. <span data-ttu-id="cdba4-109">Vælg **Styring af aktiver** > **Generelt** > **Arbejdsordrer** > **Alle arbejdsordrer** eller **Aktive arbejdsordrer**.</span><span class="sxs-lookup"><span data-stu-id="cdba4-109">Select **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="cdba4-110">Vælg arbejdsordren på listen, og vælg derefter **Budget** i gruppen **Projekt** under fanen **Arbejdsordre** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="cdba4-110">Select the work order in the list, and then, on the Action Pane > **Work order** tab > the **Project** group, select **Forecast**.</span></span> <span data-ttu-id="cdba4-111">På siden **Vedligeholdelsesprognose for arbejdsordre** vises prognoselinjer fra den type af vedligeholdelsesjob, der er valgt på arbejdsordrejobbet.</span><span class="sxs-lookup"><span data-stu-id="cdba4-111">The **Work order maintenance forecast** page shows forecast lines from the maintenance job type that is selected on the work order job.</span></span>


## <a name="add-an-hours-forecast-to-a-work-order"></a><span data-ttu-id="cdba4-112">Føje en timeprognose til en arbejdsordre</span><span class="sxs-lookup"><span data-stu-id="cdba4-112">Add an hours forecast to a work order</span></span>

1. <span data-ttu-id="cdba4-113">Vælg det arbejdsordrejob, der skal føjes et budget til, på siden **Vedligeholdelsesprognose for arbejdsordre**.</span><span class="sxs-lookup"><span data-stu-id="cdba4-113">On the **Work order maintenance forecast** page, select the work order job to add a forecast to.</span></span>

2. <span data-ttu-id="cdba4-114">I oversigtspanelet **Timer** skal du vælge **Tilføj** for at oprette en ny linje.</span><span class="sxs-lookup"><span data-stu-id="cdba4-114">On the **Hours** FastTab, select **Add** to create a new line.</span></span>

3. <span data-ttu-id="cdba4-115">Vælg en kategori i feltet **Kategori**.</span><span class="sxs-lookup"><span data-stu-id="cdba4-115">In the **Category** field, select a category.</span></span>

4. <span data-ttu-id="cdba4-116">Indsæt antal budgetterede timer i feltet **Timer**.</span><span class="sxs-lookup"><span data-stu-id="cdba4-116">In the **Hours** field, enter the number of forecasted hours.</span></span>

5. <span data-ttu-id="cdba4-117">Vælg den gebyrtype, der skal bruges på linjen, i feltet **Linjeegenskab**.</span><span class="sxs-lookup"><span data-stu-id="cdba4-117">In the **Line property** field, select the type of charge that should be used on the line.</span></span>


## <a name="add-an-items-forecast-to-a-work-order"></a><span data-ttu-id="cdba4-118">Føje en vareprognose til en arbejdsordre</span><span class="sxs-lookup"><span data-stu-id="cdba4-118">Add an items forecast to a work order</span></span>

<span data-ttu-id="cdba4-119">Du kan føje varer til en vedligeholdelsesprognose for en arbejdsordre på tre måder.</span><span class="sxs-lookup"><span data-stu-id="cdba4-119">There are three ways to add items to a work order maintenance forecast.</span></span> <span data-ttu-id="cdba4-120">Du kan oprette linjer for varer (reservedele), der ikke er medtaget på listen over reservedele eller aktivstyklisten, du kan vælge reservedele på listen over godkendte reservedele, og du kan vælge varer fra aktivstyklisten.</span><span class="sxs-lookup"><span data-stu-id="cdba4-120">You can create lines for items (spare parts) that aren't included on the spare parts list or the asset bill of materials (BOM), you can select spare parts from the approved spare parts list, or you can select items from the asset BOM.</span></span>

- <span data-ttu-id="cdba4-121">Vælg det arbejdsordrejob, hvor der skal tilføjes en prognose, på siden **Vedligeholdelsesprognose for arbejdsordre**.</span><span class="sxs-lookup"><span data-stu-id="cdba4-121">On the **Work order maintenance forecast** page, select the work order job to to add a forecast to.</span></span>

- <span data-ttu-id="cdba4-122">I oversigtspanelet **Varer** kan du føje varer til vedligeholdelsesprognosen ved at bruge den relevante metode.</span><span class="sxs-lookup"><span data-stu-id="cdba4-122">On the **Items** FastTab, add items to the maintenance forecast by using the appropriate method.</span></span>

<span data-ttu-id="cdba4-123">Følg disse trin for at oprette en ny linje til en reservedel, der ikke findes på listen over reservedele eller aktivstyklisten:</span><span class="sxs-lookup"><span data-stu-id="cdba4-123">To create a line for a spare part that isn't on the spare parts list or the asset BOM, follow these steps:</span></span>

1. <span data-ttu-id="cdba4-124">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="cdba4-124">Select **Add**.</span></span>
2. <span data-ttu-id="cdba4-125">Vælg varen i feltet **Varenummer**.</span><span class="sxs-lookup"><span data-stu-id="cdba4-125">In the **Item number** field, select the item.</span></span>
3. <span data-ttu-id="cdba4-126">Angiv antallet i feltet **Salgsantal**.</span><span class="sxs-lookup"><span data-stu-id="cdba4-126">In the **Sales quantity** field, enter the quantity.</span></span>
4. <span data-ttu-id="cdba4-127">Vælg måleenheden for antallet i feltet **Enhed**.</span><span class="sxs-lookup"><span data-stu-id="cdba4-127">In the **Unit** field, select the unit of measure for the quantity.</span></span>
5. <span data-ttu-id="cdba4-128">I felterne **Kostpris** og **Valuta** skal du angive relevante værdier.</span><span class="sxs-lookup"><span data-stu-id="cdba4-128">In the **Cost price** and **Currency** fields, enter appropriate values.</span></span>
6. <span data-ttu-id="cdba4-129">Vælg en linjeegenskab i feltet **Linjeegenskab**.</span><span class="sxs-lookup"><span data-stu-id="cdba4-129">In the **Line property** field, select a line property.</span></span>
7. <span data-ttu-id="cdba4-130">Hvis du vil ændre listen over de dimensioner, der vises på varelinjerne, skal du vælge **Lager** > **Vis dimensioner**, vælge dimensioner og indstille **Gem opsætning** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="cdba4-130">To change the list of dimensions that is shown on the item lines, select **Inventory** > **Display dimensions**, select the dimensions, and then set the **Save setup** option to **Yes**.</span></span>

<span data-ttu-id="cdba4-131">Hvis du vil tilføje en reservedel fra en godkendt reservedelsliste, skal du følge disse trin:</span><span class="sxs-lookup"><span data-stu-id="cdba4-131">To add a spare part from an approved spare parts list, follow these steps:</span></span>

1. <span data-ttu-id="cdba4-132">Vælg **Tilføj reservedele**.</span><span class="sxs-lookup"><span data-stu-id="cdba4-132">Select **Add spare parts**.</span></span>
2. <span data-ttu-id="cdba4-133">Vælg reservedelen, og rediger de relaterede oplysninger efter behov.</span><span class="sxs-lookup"><span data-stu-id="cdba4-133">Select the spare part, and edit the related information as you require.</span></span>
3. <span data-ttu-id="cdba4-134">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="cdba4-134">Select **OK**.</span></span>

<span data-ttu-id="cdba4-135">Udfør følgende trin for at tilføje en vare fra aktivstyklisten:</span><span class="sxs-lookup"><span data-stu-id="cdba4-135">To add an item from the asset BOM, follow these steps:</span></span>

1. <span data-ttu-id="cdba4-136">Vælg **Tilføj styklistevarer**.</span><span class="sxs-lookup"><span data-stu-id="cdba4-136">Select **Add BOM items**.</span></span>
2. <span data-ttu-id="cdba4-137">Vælg varen, og rediger de relaterede oplysninger efter behov.</span><span class="sxs-lookup"><span data-stu-id="cdba4-137">Select the item, and edit the related information as you require.</span></span>
3. <span data-ttu-id="cdba4-138">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="cdba4-138">Select **OK**.</span></span>

<span data-ttu-id="cdba4-139">Hvis du vil have en oversigt over, hvor varen på den valgte linje bruges i relation til aktiver,typestandarder for vedligeholdelsesjob, reservedele og arbejdsordrer i Styring af aktiver, skal du vælge **Hvor er varen brugt?**.</span><span class="sxs-lookup"><span data-stu-id="cdba4-139">To get an overview that shows where the item on the selected line is used in relation to assets, maintenance job type defaults, spare parts, and work orders in Asset Management, select **Item where used**.</span></span> <span data-ttu-id="cdba4-140">Yderligere oplysninger om denne oversigt finder du under [Hvor er varen brugt?](../controlling-and-reporting/item-where-used.md).</span><span class="sxs-lookup"><span data-stu-id="cdba4-140">For more information about this overview, see [Item where used](../controlling-and-reporting/item-where-used.md).</span></span>


## <a name="add-an-expense-forecast-to-a-work-order"></a><span data-ttu-id="cdba4-141">Føje et udgiftsbudget til en arbejdsordre</span><span class="sxs-lookup"><span data-stu-id="cdba4-141">Add an expense forecast to a work order</span></span>

1. <span data-ttu-id="cdba4-142">Vælg det arbejdsordrejob, der skal føjes et budget til, på siden **Vedligeholdelsesprognose for arbejdsordre**.</span><span class="sxs-lookup"><span data-stu-id="cdba4-142">On the **Work order maintenance forecast** page, select the work order job to add a forecast to.</span></span>

2. <span data-ttu-id="cdba4-143">I oversigtspanelet **Udgift** skal du vælge **Tilføj** for at oprette en ny linje.</span><span class="sxs-lookup"><span data-stu-id="cdba4-143">On the **Expense** FastTab, select **Add** to create a line.</span></span>

3. <span data-ttu-id="cdba4-144">Vælg en kategori i feltet **Kategori**.</span><span class="sxs-lookup"><span data-stu-id="cdba4-144">In the **Category** field, select a category.</span></span>

4. <span data-ttu-id="cdba4-145">Angiv antallet i feltet **Antal**.</span><span class="sxs-lookup"><span data-stu-id="cdba4-145">In the **Quantity** field, enter the quantity.</span></span>

5. <span data-ttu-id="cdba4-146">Indsæt relevante værdier i felterne **Kostpris**, **Salgsvaluta** og **Salgspris**.</span><span class="sxs-lookup"><span data-stu-id="cdba4-146">In the **Cost price**, **Sales currency**, and **Sales price** fields, enter appropriate values.</span></span>

6. <span data-ttu-id="cdba4-147">Vælg den gebyrtype, der skal bruges på linjen, i feltet **Linjeegenskab**.</span><span class="sxs-lookup"><span data-stu-id="cdba4-147">In the **Line property** field, select the type of charge that should be used on the line.</span></span>

>[!NOTE]
><span data-ttu-id="cdba4-148">I oversigtspanelet **Vedligeholdelsesprognosetotaler** vises en oversigt over antallet af linjer, der er oprettet for det valgte arbejdsordrejob og for arbejdsordren, i hvert oversigtspanel.</span><span class="sxs-lookup"><span data-stu-id="cdba4-148">The **Maintenance forecast totals** FastTab shows an overview of the number of lines that have been created, for the selected work order job and for the work order, on each FastTab.</span></span> <span data-ttu-id="cdba4-149">Du kan også se en total af de budgetterede arbejdstimer for arbejdsordrejobbet og arbejdsordren.</span><span class="sxs-lookup"><span data-stu-id="cdba4-149">It also shows the total forecasted work hours for the work order job and the work order.</span></span>

<span data-ttu-id="cdba4-150">I illustrationen herunder vises et eksempel på siden **Vedligeholdelsesprognose for arbejdsordre**.</span><span class="sxs-lookup"><span data-stu-id="cdba4-150">The illustration below shows an example of the **Work order maintenance forecast** page.</span></span>

![Figur 1](media/06-work-orders.png)


## <a name="automatic-update-of-work-order-forecasts"></a><span data-ttu-id="cdba4-152">Automatisk opdatering af prognoser for arbejdsordrer</span><span class="sxs-lookup"><span data-stu-id="cdba4-152">Automatic update of work order forecasts</span></span>

<span data-ttu-id="cdba4-153">I Styring af aktiver kan du automatisk opdatere eventuelle ændringer i arbejdsordrebudgetter for timeomkostninger, vareomkostninger og udgifter, der er opdateret i andre moduler i Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="cdba4-153">If hour costs, item costs, and expenses are updated in other modules in Microsoft Dynamics 365 for Finance and Operations, work order forecasts in Asset Management can automatically be updated to reflect those changes.</span></span> <span data-ttu-id="cdba4-154">Dette er med til at sikre, at de seneste kostpriser altid bruges i dine prognoser for arbejdsordrer.</span><span class="sxs-lookup"><span data-stu-id="cdba4-154">This capability helps guarantee that the latest cost prices are always used in your work order forecasts.</span></span> <span data-ttu-id="cdba4-155">Det er også muligt at foretage lignende opdateringer af [budgetter for vedligeholdelsesjobtyper](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).</span><span class="sxs-lookup"><span data-stu-id="cdba4-155">You can also do similar updates for [maintenance job type forecasts](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).</span></span>

1. <span data-ttu-id="cdba4-156">Vælg **Styring af aktiver** > **Periodisk** > **Prognose** > **Opdater prognose for arbejdsordre**.</span><span class="sxs-lookup"><span data-stu-id="cdba4-156">Select **Asset management** > **Periodic** > **Forecast** > **Update work order forecast**.</span></span>

2. <span data-ttu-id="cdba4-157">I dialogboksen **Opdater prognose for arbejdsordre** i oversigtspanelet **Poster, der skal indgå** kan du tilføje valg for bestemte arbejdsordrer eller arbejdsordrejob efter behov.</span><span class="sxs-lookup"><span data-stu-id="cdba4-157">In the **Update work order forecast** dialog, on the **Records to include** FastTab, you can add selections regarding specific work orders or work order jobs, as you require.</span></span> <span data-ttu-id="cdba4-158">Klik på **Filter** for at foretage de relevante valg.</span><span class="sxs-lookup"><span data-stu-id="cdba4-158">Click **Filter** to make the relevant selections.</span></span>

3. <span data-ttu-id="cdba4-159">I oversigtspanelet **Kør i baggrunden** kan du konfigurere automatisk opdatering som et batchjob efter behov.</span><span class="sxs-lookup"><span data-stu-id="cdba4-159">On the **Run in the background** FastTab, you can set up the automatic update as a batch job, as you require.</span></span>

4. <span data-ttu-id="cdba4-160">Vælg **OK** for at starte budgetopdateringen.</span><span class="sxs-lookup"><span data-stu-id="cdba4-160">Select **OK** to start the forecast update.</span></span>


<span data-ttu-id="cdba4-161">I illustrationen herunder vises et eksempel på dialogboksen **Opdater prognose for arbejdsordre**.</span><span class="sxs-lookup"><span data-stu-id="cdba4-161">The illustration below shows an example of the **Update work order forecast** dialog.</span></span>

![Figur 2](media/07-work-orders.png)
