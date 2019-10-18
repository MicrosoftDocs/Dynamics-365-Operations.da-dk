---
title: Vedligeholdelsesprognoser
description: I dette emne beskrives vedligeholdelsesprognoser i Styring af aktiver.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 383c910b40199f2da863144c6dc85a579d0091e9
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024493"
---
# <a name="maintenance-forecasts"></a><span data-ttu-id="f036b-103">Vedligeholdelsesprognoser</span><span class="sxs-lookup"><span data-stu-id="f036b-103">Maintenance forecasts</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="f036b-104">Når du opretter en arbejdsordre, opretter du arbejdsordrejob med relaterede aktiver og vedligeholdelsesjobtyper.</span><span class="sxs-lookup"><span data-stu-id="f036b-104">When you create a work order, you create work order jobs with related assets and maintenance job types.</span></span> <span data-ttu-id="f036b-105">Når du vælger en vedligeholdelsesjobtype, der indeholder vedligeholdelsesprognoser, kopieres prognoserne automatisk til arbejdsordren.</span><span class="sxs-lookup"><span data-stu-id="f036b-105">When you select a maintenance job type containing maintenance forecasts, the forecasts are automatically copied to the work order.</span></span>

<span data-ttu-id="f036b-106">Du kan muligvis tilføje eller slette prognoselinjer på en arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="f036b-106">You may be able to add or delete forecast lines on a work order.</span></span> <span data-ttu-id="f036b-107">Opsætningen af en livscyklustilstand for en arbejdsordre, den relaterede projekttype og stadiereglerne for projekttypen bestemmer, om du kan tilføje eller redigere prognoselinjer.</span><span class="sxs-lookup"><span data-stu-id="f036b-107">The setup of a work order lifecycle state, the related project type, and the stage rules related to the project type determines if you are able to add or edit forecast lines.</span></span> 

1. <span data-ttu-id="f036b-108">Klik på **Styring af aktiver** > **Generelt** > **Arbejdsordrer** > **Alle arbejdsordrer** eller **Aktive arbejdsordrer**.</span><span class="sxs-lookup"><span data-stu-id="f036b-108">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="f036b-109">Vælg arbejdsordren på listen, og klik på **Prognose**.</span><span class="sxs-lookup"><span data-stu-id="f036b-109">Select the work order in the list, and click **Forecast**.</span></span> <span data-ttu-id="f036b-110">I **Vedligeholdelsesprognose for arbejdsordre** vises prognoselinjer fra den type af vedligeholdelsesjob, der er valgt på arbejdsordrejobbet.</span><span class="sxs-lookup"><span data-stu-id="f036b-110">In **Work order maintenance forecast**, forecast lines from the maintenance job type selected on the work order job are displayed.</span></span>


## <a name="add-hours-forecast-to-a-work-order"></a><span data-ttu-id="f036b-111">Føje timeprognose til en arbejdsordre</span><span class="sxs-lookup"><span data-stu-id="f036b-111">Add hours forecast to a work order</span></span>

1. <span data-ttu-id="f036b-112">Vælg det arbejdsordrejob, hvor du vil tilføje en prognose.</span><span class="sxs-lookup"><span data-stu-id="f036b-112">Select the work order job to which you want to add a forecast.</span></span>

2. <span data-ttu-id="f036b-113">I oversigtspanelet **Timer** skal du klikke på **Tilføj** for at oprette en ny linje.</span><span class="sxs-lookup"><span data-stu-id="f036b-113">On the **Hours** FastTab, click **Add** to create a new line.</span></span>

3. <span data-ttu-id="f036b-114">Vælg en kategori i feltet **Kategori**.</span><span class="sxs-lookup"><span data-stu-id="f036b-114">Select a category in the **Category** field.</span></span>

4. <span data-ttu-id="f036b-115">Indsæt antal budgetterede timer i feltet **Timer**.</span><span class="sxs-lookup"><span data-stu-id="f036b-115">Insert number of forecasted hours in the **Hours** field.</span></span>

5. <span data-ttu-id="f036b-116">Vælg den gebyrtype, der skal bruges på linjen, i feltet **Linjeegenskab**.</span><span class="sxs-lookup"><span data-stu-id="f036b-116">In the **Line property** field, select the charge type to be used on the line.</span></span>


## <a name="add-items-forecast-to-a-work-order"></a><span data-ttu-id="f036b-117">Føje vareprognose til en arbejdsordre</span><span class="sxs-lookup"><span data-stu-id="f036b-117">Add items forecast to a work order</span></span>

<span data-ttu-id="f036b-118">Der er tre måder at tilføje varer i en arbejdsordres vedligeholdelsesprognose: Du kan oprette linjer for varer (reservedele), der ikke er medtaget på listen over reservedele eller aktivstyklisten, du kan vælge reservedele på listen over godkendte reservedele, og du kan vælge varer fra aktivstyklisten.</span><span class="sxs-lookup"><span data-stu-id="f036b-118">There are three ways to add items to a work order maintenance forecast: You can create lines for items (spare parts) that are not included in the spare parts list or asset BOM, you can select spare parts from the approved spare parts list, and you can select items from the asset BOM.</span></span>

1. <span data-ttu-id="f036b-119">Vælg det arbejdsordrejob, hvor du vil tilføje en prognose.</span><span class="sxs-lookup"><span data-stu-id="f036b-119">Select the work order job to which you want to add a forecast.</span></span>

2. <span data-ttu-id="f036b-120">Vælg oversigtspanelet **Varer**.</span><span class="sxs-lookup"><span data-stu-id="f036b-120">Select the **Items** FastTab.</span></span>

3. <span data-ttu-id="f036b-121">Klik på **Tilføj** for at oprette en ny linje til en reservedel, der ikke findes på listen over reservedele eller aktivstyklisten.</span><span class="sxs-lookup"><span data-stu-id="f036b-121">Click **Add** to create a new line for a spare part that is not on the spare parts list or the asset BOM list.</span></span>

4. <span data-ttu-id="f036b-122">Vælg elementet i feltet **Varenummer**.</span><span class="sxs-lookup"><span data-stu-id="f036b-122">Select the item in the **Item number** field.</span></span>

5. <span data-ttu-id="f036b-123">Indsæt antal i feltet **Salgsantal**, og vælg en antalsenhed i feltet **Enhed**.</span><span class="sxs-lookup"><span data-stu-id="f036b-123">Insert quantity in the **Sales quantity** field, and select a quantity unit in the **Unit** field.</span></span>

6. <span data-ttu-id="f036b-124">Indsæt kostpris og valuta i de relevante felter, og vælg en **Linjeegenskab**.</span><span class="sxs-lookup"><span data-stu-id="f036b-124">Insert cost price and currency in the relevant fields, and select a **Line property**.</span></span>

7. <span data-ttu-id="f036b-125">Hvis du vil ændre listen over de dimensioner, der vises på varelinjerne, skal du klikke på **Inventory** > **Vis dimensioner**, vælge dimensioner og vælge "Ja" på knappen **Gem opsætning**.</span><span class="sxs-lookup"><span data-stu-id="f036b-125">If you want to change the list of dimensions displayed on the item lines, click **Inventory** > **Display dimensions**, select the dimensions, and select "Yes" on the **Save setup** toggle button.</span></span>

8. <span data-ttu-id="f036b-126">Hvis du vil føje en godkendt reservedel til vedligeholdelsesprognosen, skal du klikke på **Tilføj reservedele**, vælge reservedelen, redigere relaterede oplysninger, hvis det er nødvendigt, og klikke på **OK**.</span><span class="sxs-lookup"><span data-stu-id="f036b-126">If you want to add an approved spare part to the maintenance forecast, click **Add spare parts**, select the spare part, edit related information if required, and click **OK**.</span></span>

9. <span data-ttu-id="f036b-127">Hvis du vil føje varer fra aktivstyklisten til prognosen, skal du klikke på **Tilføj styklistevarer**, vælge varen, redigere relaterede oplysninger, hvis det er nødvendigt, og klikke på **OK**.</span><span class="sxs-lookup"><span data-stu-id="f036b-127">If you want to add asset BOM items to the forecast, click **Add BOM items**, select the item, edit related information if required, and click **OK**.</span></span>

10. <span data-ttu-id="f036b-128">Klik på **Hvor er varen brugt?**, hvis du vil have en oversigt over, hvor i Styring af aktiver varen på den valgte linje bruges i relation til aktiver, typestandarder for vedligeholdelsesjob, reservedele og arbejdsordrer.</span><span class="sxs-lookup"><span data-stu-id="f036b-128">Click **Item where used** if you want to get an overview of where the item on the selected line is used in Asset Management in relation to assets, maintenance job type defaults, spare parts, and work orders.</span></span> 



## <a name="add-expense-forecast-to-a-work-order"></a><span data-ttu-id="f036b-129">Føje udgiftsbudget til en arbejdsordre</span><span class="sxs-lookup"><span data-stu-id="f036b-129">Add expense forecast to a work order</span></span>

1. <span data-ttu-id="f036b-130">Dette emne forklarer, hvordan du kan føje et udgiftsbudget til en arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="f036b-130">This topic explains how to add an expense forecast to a work order.</span></span> <span data-ttu-id="f036b-131">I venstre side af formen skal du vælge det arbejdsordrejob, hvor du vil tilføje et budget.</span><span class="sxs-lookup"><span data-stu-id="f036b-131">In the left-hand side of the form, select the work order job to which you want to add a forecast.</span></span>

2. <span data-ttu-id="f036b-132">Vælg oversigtspanelet **Udgift**.</span><span class="sxs-lookup"><span data-stu-id="f036b-132">Select the **Expense** FastTab.</span></span>

3. <span data-ttu-id="f036b-133">Klik på **Tilføj** for at oprette en ny linje.</span><span class="sxs-lookup"><span data-stu-id="f036b-133">Click **Add** to create a new line.</span></span>

4. <span data-ttu-id="f036b-134">Vælg en kategori i feltet **Kategori**.</span><span class="sxs-lookup"><span data-stu-id="f036b-134">Select a category in the **Category** field.</span></span>

5. <span data-ttu-id="f036b-135">Angiv antallet i feltet **Antal**.</span><span class="sxs-lookup"><span data-stu-id="f036b-135">Insert quantity in the **Quantity** field.</span></span>

6. <span data-ttu-id="f036b-136">Indsæt kostpris, salgsvaluta og salgspris i de relevante felter.</span><span class="sxs-lookup"><span data-stu-id="f036b-136">Insert cost price, sales currency, and sales price in the relevant fields.</span></span>

7. <span data-ttu-id="f036b-137">Vælg den gebyrtype, der skal bruges på linjen, i feltet **Linjeegenskab**.</span><span class="sxs-lookup"><span data-stu-id="f036b-137">In the **Line property** field, select the charge type to be used on the line.</span></span>

>[!NOTE]
><span data-ttu-id="f036b-138">I oversigtspanelet **Vedligeholdelsesprognosetotaler** kan du få vist en oversigt over antallet af linjer, der er oprettet under hver fane, for det valgte arbejdsordrejob og for arbejdsordren.</span><span class="sxs-lookup"><span data-stu-id="f036b-138">On the **Maintenance forecast totals** FastTab, you can see an overview of the number of lines created on each tab, for the selected work order job and for the work order.</span></span> <span data-ttu-id="f036b-139">Du kan også se en sum af de budgetterede arbejdstimer for arbejdsordrejobbet og for arbejdsordren.</span><span class="sxs-lookup"><span data-stu-id="f036b-139">Also, you can see a sum of forecasted work hours for the work order job and for the work order.</span></span>

![Figur 1](media/06-work-orders.png)


## <a name="automatic-update-of-work-order-forecasts"></a><span data-ttu-id="f036b-141">Automatisk opdatering af prognoser for arbejdsordrer</span><span class="sxs-lookup"><span data-stu-id="f036b-141">Automatic update of work order forecasts</span></span>

<span data-ttu-id="f036b-142">I Styring af aktiver kan du automatisk opdatere eventuelle ændringer i arbejdsordrebudgetter for timeomkostninger, vareomkostninger og udgifter, der er opdateret i andre moduler.</span><span class="sxs-lookup"><span data-stu-id="f036b-142">In Asset Management, you can automatically update any changes in work order forecasts regarding hour costs, item costs, and expenses, which have been updated in other modules.</span></span> <span data-ttu-id="f036b-143">Dette gøres for at sikre, at de seneste kostpriser altid bruges i dine prognoser for arbejdsordrer.</span><span class="sxs-lookup"><span data-stu-id="f036b-143">This is done to ensure that the latest cost prices are always used in your work order forecasts.</span></span> <span data-ttu-id="f036b-144">Det er også muligt at foretage lignende opdateringer af [budgetter for vedligeholdelsesjobtyper](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).</span><span class="sxs-lookup"><span data-stu-id="f036b-144">It is also possible to make similar updates for [maintenance job type forecasts](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).</span></span>

1. <span data-ttu-id="f036b-145">Klik på **Styring af aktiver** > **Periodisk** > **Prognose** > **Opdater prognose for arbejdsordre**.</span><span class="sxs-lookup"><span data-stu-id="f036b-145">Click **Asset management** > **Periodic** > **Forecast** > **Update work order forecast**.</span></span>

2. <span data-ttu-id="f036b-146">I dialogboksen **Opdater prognose for arbejdsordre** kan du tilføje valg for bestemte arbejdsordrer eller arbejdsordrejob, hvis det er nødvendigt.</span><span class="sxs-lookup"><span data-stu-id="f036b-146">In the **Update work order forecast** drop-down dialog, you can add selections regarding specific work orders or work order jobs, if required.</span></span> <span data-ttu-id="f036b-147">Klik på **Filter** for at foretage disse valg.</span><span class="sxs-lookup"><span data-stu-id="f036b-147">Click **Filter** to make those selections.</span></span>

3. <span data-ttu-id="f036b-148">I oversigtspanelet **Kør i baggrunden** kan du konfigurere automatisk opdatering som et batchjob efter behov.</span><span class="sxs-lookup"><span data-stu-id="f036b-148">If required, you can set up the automatic update as a batch job on the **Run in the background** FastTab.</span></span>

4. <span data-ttu-id="f036b-149">Klik på **OK** for at starte prognoseopdateringen.</span><span class="sxs-lookup"><span data-stu-id="f036b-149">Click **OK** to start the forecast update.</span></span>


![Figur 2](media/07-work-orders.png)

