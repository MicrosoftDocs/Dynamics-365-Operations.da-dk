---
title: Dato- og omkostningsstyring
description: I dette emne beskrives omkostnings- og datostyring i Styring af aktiver.
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetBICostControlWorkspace, EntAssetWorkOrderDateControl, EntAssetWorkOrderForecastCostInfoPart, EntAssetMaintenanceCostTrans, EntAssetWorkOrderDateControlCalcDialog, EntAssetCostControl, EntAssetCostObjectCalendar, EntAssetWorkOrderCostInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1de12233ff296f77ba9984fa8d957d4c2bc90b3f
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/16/2021
ms.locfileid: "5019069"
---
# <a name="cost-and-date-control"></a><span data-ttu-id="78283-103">Dato- og omkostningsstyring</span><span class="sxs-lookup"><span data-stu-id="78283-103">Cost and date control</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="78283-104">I Styring af aktiver kan du beregne omkostninger for at få et overblik over de faktiske omkostninger i forhold til budgetterede omkostninger på aktiver, arbejdssteder og arbejdsordrer.</span><span class="sxs-lookup"><span data-stu-id="78283-104">In Asset Management, you can calculate costs to get an overview of actual costs compared to budget costs on assets, functional locations, and work orders.</span></span> <span data-ttu-id="78283-105">De faktiske omkostninger er baseret på bogførte transaktioner.</span><span class="sxs-lookup"><span data-stu-id="78283-105">Actual costs are based on posted transactions.</span></span> 

<span data-ttu-id="78283-106">Du kan også foretage en datoberegning, hvis du vil sammenligne planlagte start- og slutdatoer med faktiske start- og slutdatoer på arbejdsordrer.</span><span class="sxs-lookup"><span data-stu-id="78283-106">You can also make a date calculation if you want to compare scheduled start and end dates to actual start and end dates on work orders.</span></span>

## <a name="cost-control-for-assets-functional-locations-and-work-orders"></a><span data-ttu-id="78283-107">Omkostningsstyring for aktiver, arbejdssteder og arbejdsordrer</span><span class="sxs-lookup"><span data-stu-id="78283-107">Cost control for assets, functional locations, and work orders</span></span>

<span data-ttu-id="78283-108">De beregninger, der foretages for aktiver, arbejdssteder og arbejdsordrer, er næsten identiske.</span><span class="sxs-lookup"><span data-stu-id="78283-108">The calculations made for assets, functional locations, and work orders are almost identical.</span></span> <span data-ttu-id="78283-109">Den eneste forskel er, at for aktiver og arbejdssteder kan du også medtage underaktiver og underordnede arbejdssteder i beregningen.</span><span class="sxs-lookup"><span data-stu-id="78283-109">The only difference is that for assets and functional locations, you can also include sub assets and sub locations in your calculation.</span></span> <span data-ttu-id="78283-110">Datoen er den transaktionsdato, da registreringen blev foretaget.</span><span class="sxs-lookup"><span data-stu-id="78283-110">The date is the transaction date when the registration was recorded.</span></span>

1. <span data-ttu-id="78283-111">Klik på **Styring af aktiver** > **Forespørgsler** > **Aktiver** > **Omkostningsstyring for aktiv** eller **Omkostningsstyring for arbejdssted** eller **Styring af aktiver** > **Forespørgsler** > **Arbejdsordrer** > **Omkostningsstyring for arbejdsordre**.</span><span class="sxs-lookup"><span data-stu-id="78283-111">Click **Asset management** > **Inquiries** > **Assets** > **Asset cost control** or **Functional location cost control**, or **Asset management** > **Inquiries** > **Work orders** > **Work order cost control**.</span></span>

2. <span data-ttu-id="78283-112">Vælg et tidsinterval, der skal beregnes, i **Omkostningsstyring for aktiv** / **Omkostningsstyring for arbejdssted** / **Omkostningsstyring for arbejdsordre**.</span><span class="sxs-lookup"><span data-stu-id="78283-112">In the **Asset cost control** / **Functional location cost control** / **Work order cost control** dialog, select a time range to be calculated.</span></span>

3. <span data-ttu-id="78283-113">Hvis det er nødvendigt, skal du vælge en økonomisk dimensionsopsætning, der skal medtages i beregningen.</span><span class="sxs-lookup"><span data-stu-id="78283-113">If required, select a financial dimension set to be included in the calculation.</span></span>

4. <span data-ttu-id="78283-114">Vælg "Ja" på til/fra-knappen **Spring over nul**, hvis du ikke vil have vist resultater med en omkostning på nul.</span><span class="sxs-lookup"><span data-stu-id="78283-114">Select "Yes" on the **Skip zero** toggle button if you don't want to show results with a cost of zero.</span></span>

5. <span data-ttu-id="78283-115">Du kan bruge feltet **Niveau** til at angive, hvor detaljerede omkostningsstyringslinjerne skal være i forbindelse med arbejdssteder.</span><span class="sxs-lookup"><span data-stu-id="78283-115">You can use the **Level** field to indicate how detailed you want the cost control lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="78283-116">Hvis du f.eks. indsætter tallet "1" i feltet, og du har et arbejdsstedshierarki med flere niveauer, vises alle omkostningsstyringslinjer for et arbejdssted på det øverste niveau, og derfor kan timerne på en linje være opsummeret fra arbejdssteder, der findes på et lavere niveau.</span><span class="sxs-lookup"><span data-stu-id="78283-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location hierarchy, all cost control lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
    
    <span data-ttu-id="78283-117">Hvis du indsætter tallet "0" i feltet **Niveau**, kan du se et detaljeret resultat, der viser alle omkostningsstyringslinjer på alle de arbejdsstedsniveauer, de er relateret til.</span><span class="sxs-lookup"><span data-stu-id="78283-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all cost control lines on all the functional location level to which they are related.</span></span>

6. <span data-ttu-id="78283-118">Vælg "Ja" på knappen **Vis åben bindende omkostning**, hvis du vil medtage denne kolonne i beregningen.</span><span class="sxs-lookup"><span data-stu-id="78283-118">Select "Yes" on the **Show open committed cost** toggle button if you want to include that column in the calculation.</span></span>

7. <span data-ttu-id="78283-119">Vælg "Ja" i til/fra-knappen **Medtag underaktiver** for at få vist omkostninger, der er relateret til underaktiver som separate linjer.</span><span class="sxs-lookup"><span data-stu-id="78283-119">Select "Yes" on the **Include sub assets** toggle button to show costs related to sub assets as separate lines.</span></span>

8. <span data-ttu-id="78283-120">Hvis du vil begrænse søgningen, kan du vælge bestemte aktiver / arbejdssteder / arbejdsordrer i oversigtspanelet **Poster, der skal indgå**.</span><span class="sxs-lookup"><span data-stu-id="78283-120">If you want to limit the search, you can select specific assets / functional locations / work orders on the **Records to include** FastTab.</span></span>

9. <span data-ttu-id="78283-121">Klik på **OK** for at starte beregningen.</span><span class="sxs-lookup"><span data-stu-id="78283-121">Click **OK** to start the calculation.</span></span>

    <span data-ttu-id="78283-122">I figuren herunder vises et eksempel på dialogboksen **Omkostningsstyring for aktiv**.</span><span class="sxs-lookup"><span data-stu-id="78283-122">The figure below shows an example of the **Asset cost control** dialog.</span></span>

    ![Dialogboksen Omkostningsstyring for aktiv](media/01-controlling-and-reporting.png)

10. <span data-ttu-id="78283-124">Klik på **Sammenlæg pr.**-knapperne på siden **Omkostningsstyring for aktiv** for at få vist det nødvendige detaljeringsniveau i beregningen.</span><span class="sxs-lookup"><span data-stu-id="78283-124">On the **Asset cost control** page, click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="78283-125">De valgte **Sammenlæg pr.**-knapper er fremhævet.</span><span class="sxs-lookup"><span data-stu-id="78283-125">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="78283-126">Klik på en knap for at aktivere eller deaktivere den.</span><span class="sxs-lookup"><span data-stu-id="78283-126">Click on a button to activate or deactivate it.</span></span>

## <a name="example"></a><span data-ttu-id="78283-127">Eksempel</span><span class="sxs-lookup"><span data-stu-id="78283-127">Example</span></span>

<span data-ttu-id="78283-128">I skærmbilledet herunder vises et eksempel på beregningsresultater i **Omkostningsstyring for aktiv**.</span><span class="sxs-lookup"><span data-stu-id="78283-128">The screenshot below shows an example of calculation results in **Asset cost control**.</span></span>

- <span data-ttu-id="78283-129">I feltet **Oprindeligt budget** vises budgetomkostninger fra arbejdsordrebudgettet.</span><span class="sxs-lookup"><span data-stu-id="78283-129">The **Original budget** field shows budget costs from the work order forecast.</span></span> 
- <span data-ttu-id="78283-130">Feltet **Bindende omkostning** viser det samlede udgiftsbeløb, som en juridisk enhed har bundet sig til at betale.</span><span class="sxs-lookup"><span data-stu-id="78283-130">The **Committed cost** field shows the total amount of expenses that a legal entity has committed itself to pay.</span></span> 
- <span data-ttu-id="78283-131">Feltet **Åben bindende omkostning** viser forpligtelser til at betale for varer, timer og tjenester, du har bestilt eller modtaget, men endnu ikke betalt for.</span><span class="sxs-lookup"><span data-stu-id="78283-131">The **Open committed cost** field shows commitments to pay for items, hours, and services you have ordered or received but not yet paid for.</span></span> 
- <span data-ttu-id="78283-132">Når alle forbrugsregistreringer er bogført, vises de tilknyttede omkostninger i feltet **Faktiske omkostninger**.</span><span class="sxs-lookup"><span data-stu-id="78283-132">The **Actual cost** field shows related costs after all consumption registrations have been posted.</span></span>

![Eksempel på beregningsresultater i Omkostningsstyring for aktiv](media/02-controlling-and-reporting.png)

<span data-ttu-id="78283-134">Du kan også foretage en omkostningsberegning ved at vælge flere aktiver i **Alle aktiver** eller **Aktive aktiver**.</span><span class="sxs-lookup"><span data-stu-id="78283-134">Another way of making a cost calculation is to multi-select assets in **All assets** or **Active assets**.</span></span> <span data-ttu-id="78283-135">Derefter skal du klikke på knappen **Omkostningsstyring** under fanen **Generelt**. I dialogboksen **Omkostningsstyring for aktiv** indsættes de valgte aktiver automatisk i feltet **Aktiv** i oversigtspanelet **Poster, der skal indgå**.</span><span class="sxs-lookup"><span data-stu-id="78283-135">Then, you click the **Cost control** button on the **General** tab. In the **Asset cost control** dialog, the selected assets are automatically inserted in the **Asset** field on the **Records to include** FastTab.</span></span> <span data-ttu-id="78283-136">Klik på **OK**, så der vises en omkostningsberegning for de valgte aktiver.</span><span class="sxs-lookup"><span data-stu-id="78283-136">Click **OK**, and a cost calculation for the selected assets is shown.</span></span> <span data-ttu-id="78283-137">Den samme procedure kan udføres for arbejdssteder i **Alle arbejdssteder** eller **Aktive arbejdssteder** og for arbejdsordrer i **Alle arbejdsordrer** eller **Aktive arbejdsordrer**.</span><span class="sxs-lookup"><span data-stu-id="78283-137">The same procedure can be done for functional locations in **All functional locations** or **Active functional locations**, and for work orders in **All work orders** or **Active work orders**.</span></span>


## <a name="work-order-date-control"></a><span data-ttu-id="78283-138">Datokontrol af arbejdsordre</span><span class="sxs-lookup"><span data-stu-id="78283-138">Work order date control</span></span>

<span data-ttu-id="78283-139">Brug denne side til at få en oversigt over forventede start- og slutdatoer sammenlignet med faktiske start- og slutdatoer på arbejdsordrer.</span><span class="sxs-lookup"><span data-stu-id="78283-139">Use this page to get an overview of expected start and end dates compared to actual start and end dates on work orders.</span></span>

1. <span data-ttu-id="78283-140">Klik på **Styring af aktiver** > **Forespørgsler** > **Arbejdsordrer** > **Datostyring af arbejdsordre**.</span><span class="sxs-lookup"><span data-stu-id="78283-140">Click **Asset management** > **Inquiries** > **Work orders** > **Work order date control**.</span></span>

2. <span data-ttu-id="78283-141">Klik på **Beregn**.</span><span class="sxs-lookup"><span data-stu-id="78283-141">Click **Calculate**.</span></span>

3. <span data-ttu-id="78283-142">I feltet **Arbejdssted** skal du vælge et arbejdssted.</span><span class="sxs-lookup"><span data-stu-id="78283-142">Select a functional location in the **Functional location** field.</span></span>

4. <span data-ttu-id="78283-143">Indsæt det interval, du vil foretage beregningen for, i felterne **Fra-dato** og **Til-dato**.</span><span class="sxs-lookup"><span data-stu-id="78283-143">Insert the range for which you want to make the calculation in the **From date** and **To date** fields.</span></span> <span data-ttu-id="78283-144">Alle de arbejdsordrer, der har forventet startdato i intervallet, vil blive medtaget.</span><span class="sxs-lookup"><span data-stu-id="78283-144">All work orders with expected start date within the range will be included.</span></span>

5. <span data-ttu-id="78283-145">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="78283-145">Click **OK**.</span></span>

6. <span data-ttu-id="78283-146">Klik på **Sammenlæg pr.**-knapper for at få vist det nødvendige detaljeringsniveau i beregningen.</span><span class="sxs-lookup"><span data-stu-id="78283-146">Click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="78283-147">De valgte **Sammenlæg pr.**-knapper er fremhævet.</span><span class="sxs-lookup"><span data-stu-id="78283-147">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="78283-148">Klik på en knap for at aktivere eller deaktivere den.</span><span class="sxs-lookup"><span data-stu-id="78283-148">Click on a button to activate or deactivate it.</span></span>

## <a name="example"></a><span data-ttu-id="78283-149">Eksempel</span><span class="sxs-lookup"><span data-stu-id="78283-149">Example</span></span>

<span data-ttu-id="78283-150">I skærmbilledet herunder vises et eksempel på beregningsresultater i **Datostyring af arbejdsordre**.</span><span class="sxs-lookup"><span data-stu-id="78283-150">The screenshot below shows an example of calculation results in **Work order date control**.</span></span>

- <span data-ttu-id="78283-151">Feltet **Gns. startforsinkelse** viser forskellen i dage mellem den planlagte startdato for en arbejdsordre sammenlignet med den faktiske startdato.</span><span class="sxs-lookup"><span data-stu-id="78283-151">The **Avg. start delay** field shows the difference in days between scheduled start date for a work order compared to actual start date.</span></span> <span data-ttu-id="78283-152">Hvis den faktiske startdato f.eks. er to dage før den planlagte startdato, vises "-2" i dette felt.</span><span class="sxs-lookup"><span data-stu-id="78283-152">If, for example, the actual start date was two days before the scheduled start date, "-2" will be displayed in this field.</span></span>  
- <span data-ttu-id="78283-153">Feltet **Gns. slutforsinkelse** viser forskellen i dage mellem den planlagte slutdato for en arbejdsordre sammenlignet med den faktiske slutdato.</span><span class="sxs-lookup"><span data-stu-id="78283-153">The **Avg. end delay** field shows the difference in days between scheduled end date for a work order compared to actual end date.</span></span> <span data-ttu-id="78283-154">Hvis den faktiske slutdato f.eks. er tre dage efter den planlagte slutdato, vises "3" i dette felt.</span><span class="sxs-lookup"><span data-stu-id="78283-154">If, for example, the actual end date was three days after the scheduled end date, "3" will be displayed in this field.</span></span>  
- <span data-ttu-id="78283-155">Felterne **Forekomster** viser antallet af gange, som afvigelser forekommer vedrørende planlagt og faktisk startdato samt planlagt og faktisk slutdato for arbejdsordren.</span><span class="sxs-lookup"><span data-stu-id="78283-155">The **Occurrences** fields show the number of times deviations occur in relation to scheduled and actual start date, and scheduled and actual end date on the work order.</span></span>

![Eksempel på beregningsresultater i Datostyring af arbejdsordre](media/03-controlling-and-reporting.png)


