---
title: Dato- og omkostningsstyring
description: I dette emne beskrives omkostnings- og datostyring i Styring af aktiver.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
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
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2bcd1584f6a858f7589387fbfe96267b7c16176a
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918389"
---
# <a name="cost-and-date-control"></a><span data-ttu-id="88a26-103">Dato- og omkostningsstyring</span><span class="sxs-lookup"><span data-stu-id="88a26-103">Cost and date control</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="88a26-104">I Styring af aktiver kan du beregne omkostninger for at få et overblik over de faktiske omkostninger i forhold til budgetterede omkostninger på aktiver, arbejdssteder og arbejdsordrer.</span><span class="sxs-lookup"><span data-stu-id="88a26-104">In Asset Management, you can calculate costs to get an overview of actual costs compared to budget costs on assets, functional locations, and work orders.</span></span> <span data-ttu-id="88a26-105">De faktiske omkostninger er baseret på bogførte transaktioner.</span><span class="sxs-lookup"><span data-stu-id="88a26-105">Actual costs are based on posted transactions.</span></span> <span data-ttu-id="88a26-106">Du kan også foretage en datoberegning, hvis du vil sammenligne planlagte start- og slutdatoer med faktiske start- og slutdatoer på arbejdsordrer.</span><span class="sxs-lookup"><span data-stu-id="88a26-106">You can also make a date calculation if you want to compare scheduled start and end dates to actual start and end dates on work orders.</span></span>

## <a name="cost-control-for-assets-functional-locations-and-work-orders"></a><span data-ttu-id="88a26-107">Omkostningsstyring for aktiver, arbejdssteder og arbejdsordrer</span><span class="sxs-lookup"><span data-stu-id="88a26-107">Cost control for assets, functional locations, and work orders</span></span>

<span data-ttu-id="88a26-108">De beregninger, der foretages for aktiver, arbejdssteder og arbejdsordrer, er næsten identiske.</span><span class="sxs-lookup"><span data-stu-id="88a26-108">The calculations made for assets, functional locations, and work orders are almost identical.</span></span> <span data-ttu-id="88a26-109">Den eneste forskel er, at for aktiver og arbejdssteder kan du også medtage underaktiver og underordnede arbejdssteder i beregningen.</span><span class="sxs-lookup"><span data-stu-id="88a26-109">Only difference is that for assets and functional locations, you can also include sub assets and sub locations in your calculation.</span></span> <span data-ttu-id="88a26-110">Datoen er den transaktionsdato, da registreringen blev foretaget.</span><span class="sxs-lookup"><span data-stu-id="88a26-110">The date is the transaction date when the registration was recorded.</span></span>

1. <span data-ttu-id="88a26-111">Klik på **Styring af aktiver** > **Forespørgsler** > **Aktiver** > **Omkostningsstyring for aktiv** eller **Omkostningsstyring for arbejdssted** eller **Styring af aktiver** > **Forespørgsler** > **Arbejdsordrer** > **Omkostningsstyring for arbejdsordre**.</span><span class="sxs-lookup"><span data-stu-id="88a26-111">Click **Asset management** > **Inquiries** > **Assets** > **Asset cost control** or **Functional location cost control**, or **Asset management** > **Inquiries** > **Work orders** > **Work order cost control**.</span></span>

2. <span data-ttu-id="88a26-112">Vælg en periode, der skal beregnes, i **Omkostningsstyring for aktiv** / **Omkostningsstyring for arbejdssted** / **Omkostningsstyring for arbejdsordre**.</span><span class="sxs-lookup"><span data-stu-id="88a26-112">In the **Asset cost control** / **Functional location cost control** / **Work order cost control** dialog, select a period to be calculated.</span></span>

3. <span data-ttu-id="88a26-113">Hvis det er nødvendigt, skal du vælge en økonomisk dimensionsopsætning, der skal medtages i beregningen.</span><span class="sxs-lookup"><span data-stu-id="88a26-113">If required, select a financial dimension set to be included in the calculation.</span></span>

4. <span data-ttu-id="88a26-114">Vælg "Ja" på til/fra-knappen **Spring over nul**, hvis du ikke vil have vist resultater med en omkostning på nul.</span><span class="sxs-lookup"><span data-stu-id="88a26-114">Select "Yes" on the **Skip zero** toggle button if you don't want to show results with a cost of zero.</span></span>

5. <span data-ttu-id="88a26-115">Du kan bruge feltet **Niveau** til at angive, hvor detaljerede omkostningsstyringslinjerne skal være i forbindelse med arbejdssteder.</span><span class="sxs-lookup"><span data-stu-id="88a26-115">You can use the **Level** field to indicate how detailed you want the cost control lines to be regarding functional locations.</span></span> <span data-ttu-id="88a26-116">Hvis du f.eks. indsætter tallet "1" i feltet, og du har et arbejdsstedshierarki med flere niveauer, vises alle omkostningsstyringslinjer for et arbejdssted på det øverste niveau, og derfor kan timerne på en linje være opsummeret fra arbejdssteder, der findes på et lavere niveau.</span><span class="sxs-lookup"><span data-stu-id="88a26-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location hierarchy, all cost control lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="88a26-117">Hvis du indsætter tallet "0" i feltet **Niveau**, kan du se et detaljeret resultat, der viser alle omkostningsstyringslinjer på alle de arbejdsstedsniveauer, de er relateret til.</span><span class="sxs-lookup"><span data-stu-id="88a26-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all cost control lines on all the functional location level to which they are related.</span></span>

6. <span data-ttu-id="88a26-118">Vælg "Ja" på knappen **Vis åben bindende omkostning**, hvis du vil medtage denne kolonne i beregningen.</span><span class="sxs-lookup"><span data-stu-id="88a26-118">Select "Yes" on the **Show open committed cost** toggle button if you want to include that column in the calculation.</span></span>

7. <span data-ttu-id="88a26-119">Vælg "Ja" i til/fra-knappen **Medtag underaktiver** for at få vist omkostninger, der er relateret til underaktiver som separate linjer.</span><span class="sxs-lookup"><span data-stu-id="88a26-119">Select "Yes" on the **Include sub assets** toggle button to show costs related to sub assets as separate lines.</span></span>

8. <span data-ttu-id="88a26-120">Hvis du vil begrænse søgningen, kan du vælge bestemte aktiver / arbejdssteder / arbejdsordrer i oversigtspanelet **Poster, der skal indgå**.</span><span class="sxs-lookup"><span data-stu-id="88a26-120">If you want to limit the search, you can select specific assets / functional locations / work orders on the **Records to include** FastTab.</span></span>

9. <span data-ttu-id="88a26-121">Klik på **OK** for at starte beregningen.</span><span class="sxs-lookup"><span data-stu-id="88a26-121">Click **OK** to start the calculation.</span></span>

<span data-ttu-id="88a26-122">I figuren herunder vises et eksempel på dialogboksen **Omkostningsstyring for aktiv**.</span><span class="sxs-lookup"><span data-stu-id="88a26-122">The figure below shows an example of the **Asset cost control** dialog.</span></span>

![Figur 1](media/01-controlling-and-reporting.png)

10. <span data-ttu-id="88a26-124">På siden **Omkostningsstyring for aktiv** i **Gruppér efter...**-handlingsrudegrupper skal du klikke på de relevante knapper for at få vist det nødvendige detaljeringsniveau i beregningen.</span><span class="sxs-lookup"><span data-stu-id="88a26-124">In the **Group by...** action pane groups on the **Asset cost control** page, click the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="88a26-125">De valgte handlingsrudeknapper er fremhævet.</span><span class="sxs-lookup"><span data-stu-id="88a26-125">The selected action pane buttons are highlighted.</span></span> <span data-ttu-id="88a26-126">Klik på en knap for at aktivere eller deaktivere den.</span><span class="sxs-lookup"><span data-stu-id="88a26-126">Click on a button to activate or deactivate it.</span></span>

<span data-ttu-id="88a26-127">I figuren herunder vises et eksempel på beregningsresultater i **Omkostningsstyring for aktiv**.</span><span class="sxs-lookup"><span data-stu-id="88a26-127">The figure below shows an example of calculation results in **Asset cost control**.</span></span>

![Figur 2](media/02-controlling-and-reporting.png)

<span data-ttu-id="88a26-129">Du kan også foretage en omkostningsberegning ved at vælge flere aktiver i **Alle aktiver** eller **Aktive aktiver**.</span><span class="sxs-lookup"><span data-stu-id="88a26-129">Another way of making a cost calculation is to multi-select assets in **All assets** or **Active assets**.</span></span> <span data-ttu-id="88a26-130">Derefter skal du klikke på knappen **Omkostningsstyring** under fanen **Generelt**. I dialogboksen **Omkostningsstyring for aktiv** indsættes de valgte aktiver automatisk i feltet **Aktiv** i oversigtspanelet **Poster, der skal indgå**.</span><span class="sxs-lookup"><span data-stu-id="88a26-130">Then, you click the **Cost control** button on the **General** tab. In the **Asset cost control** dialog, the selected assets are automatically inserted in the **Asset** field on the **Records to include** FastTab.</span></span> <span data-ttu-id="88a26-131">Klik på **OK**, så der vises en omkostningsberegning for de valgte aktiver.</span><span class="sxs-lookup"><span data-stu-id="88a26-131">Click **OK**, and a cost calculation for the selected assets is shown.</span></span> <span data-ttu-id="88a26-132">Den samme procedure kan udføres for arbejdssteder i **Alle arbejdssteder** eller **Aktive arbejdssteder** og for arbejdsordrer i **Alle arbejdsordrer** eller **Aktive arbejdsordrer**.</span><span class="sxs-lookup"><span data-stu-id="88a26-132">The same procedure can be done for functional locations in **All functional locations** or **Active functional locations**, and for work orders in **All work orders** or **Active work orders**.</span></span>

>[!NOTE]
><span data-ttu-id="88a26-133">I feltet **Oprindeligt budget** vises budgetomkostninger fra arbejdsordrebudgettet.</span><span class="sxs-lookup"><span data-stu-id="88a26-133">The **Original budget** field shows budget costs from the work order forecast.</span></span> <span data-ttu-id="88a26-134">Feltet **Bindende omkostning** viser det samlede udgiftsbeløb, som en juridisk enhed har bundet sig til at betale.</span><span class="sxs-lookup"><span data-stu-id="88a26-134">The **Committed cost** field shows the total amount of expenses that a legal entity has committed itself to pay.</span></span> <span data-ttu-id="88a26-135">Feltet **Åben bindende omkostning** viser forpligtelser til at betale for varer, timer og tjenester, du har bestilt eller modtaget, men endnu ikke betalt for.</span><span class="sxs-lookup"><span data-stu-id="88a26-135">The **Open committed cost** field shows commitments to pay for items, hours, and services you have ordered or received but not yet paid for.</span></span> <span data-ttu-id="88a26-136">Når alle forbrugsregistreringer er bogført, medtages de tilknyttede omkostninger i feltet **Faktiske omkostninger**.</span><span class="sxs-lookup"><span data-stu-id="88a26-136">When all consumption registrations have been posted, the related costs are included in the **Actual cost** field.</span></span>

## <a name="work-order-date-control"></a><span data-ttu-id="88a26-137">Datokontrol af arbejdsordre</span><span class="sxs-lookup"><span data-stu-id="88a26-137">Work order date control</span></span>

<span data-ttu-id="88a26-138">Brug denne side til at få en oversigt over forventede start- og slutdatoer sammenlignet med faktiske start- og slutdatoer på arbejdsordrer.</span><span class="sxs-lookup"><span data-stu-id="88a26-138">Use this page to get an overview of expected start and end dates compared to actual start and end dates on work orders.</span></span>

1. <span data-ttu-id="88a26-139">Klik på **Styring af aktiver** > **Forespørgsler** > **Arbejdsordrer** > **Datostyring af arbejdsordre**.</span><span class="sxs-lookup"><span data-stu-id="88a26-139">Click **Asset management** > **Inquiries** > **Work orders** > **Work order date control**.</span></span>

2. <span data-ttu-id="88a26-140">Klik på **Beregn**.</span><span class="sxs-lookup"><span data-stu-id="88a26-140">Click **Calculate**.</span></span>

3. <span data-ttu-id="88a26-141">I feltet **Arbejdssted** skal du vælge et arbejdssted.</span><span class="sxs-lookup"><span data-stu-id="88a26-141">Select a functional location in the **Functional location** field.</span></span>

4. <span data-ttu-id="88a26-142">Indsæt den periode, du vil foretage beregningen for, i felterne **Fra-dato** og **Til-dato**.</span><span class="sxs-lookup"><span data-stu-id="88a26-142">Insert the period for which you want to make the calculation in the **From date** and **To date** fields.</span></span> <span data-ttu-id="88a26-143">Alle de arbejdsordrer, der har forventet start i perioden, vil blive medtaget.</span><span class="sxs-lookup"><span data-stu-id="88a26-143">All work orders with expected start within the period will be included.</span></span>

5. <span data-ttu-id="88a26-144">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="88a26-144">Click **OK**.</span></span>

6. <span data-ttu-id="88a26-145">I **Sammenlæg pr.**-handlingsrudegrupperne skal du klikke på de relevante knapper for at få vist det nødvendige detaljeringsniveau i beregningen.</span><span class="sxs-lookup"><span data-stu-id="88a26-145">In the **Group by...** action pane groups, click the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="88a26-146">De valgte handlingsrudeknapper er fremhævet.</span><span class="sxs-lookup"><span data-stu-id="88a26-146">The selected action pane buttons are highlighted.</span></span> <span data-ttu-id="88a26-147">Klik på en knap for at aktivere eller deaktivere den.</span><span class="sxs-lookup"><span data-stu-id="88a26-147">Click on a button to activate or deactivate it.</span></span>

<span data-ttu-id="88a26-148">I figuren herunder vises et eksempel på beregningsresultater i **Datostyring af arbejdsordre**.</span><span class="sxs-lookup"><span data-stu-id="88a26-148">The figure below shows an example of calculation results in **Work order date control**.</span></span>

![Figur 3](media/03-controlling-and-reporting.png)

- <span data-ttu-id="88a26-150">Feltet **Gns. startforsinkelse** viser forskellen i dage mellem den planlagte startdato for en arbejdsordre sammenlignet med den faktiske startdato.</span><span class="sxs-lookup"><span data-stu-id="88a26-150">The **Avg. start delay** field shows the difference in days between scheduled start date for a work order compared to actual start date.</span></span> <span data-ttu-id="88a26-151">Hvis den faktiske startdato f.eks. er to dage før den planlagte startdato, vises "-2" i dette felt.</span><span class="sxs-lookup"><span data-stu-id="88a26-151">If, for example, the actual start date was two days before the scheduled start date, "-2" will be displayed in this field.</span></span>  
- <span data-ttu-id="88a26-152">Feltet **Gns. slutforsinkelse** viser forskellen i dage mellem den planlagte slutdato for en arbejdsordre sammenlignet med den faktiske slutdato.</span><span class="sxs-lookup"><span data-stu-id="88a26-152">The **Avg. end delay** field shows the difference in days between scheduled end date for a work order compared to actual end date.</span></span> <span data-ttu-id="88a26-153">Hvis den faktiske slutdato f.eks. er tre dage efter den planlagte slutdato, vises "3" i dette felt.</span><span class="sxs-lookup"><span data-stu-id="88a26-153">If, for example, the actual end date was three days after the scheduled end date, "3" will be displayed in this field.</span></span>  
- <span data-ttu-id="88a26-154">Felterne **Forekomster** viser antallet af gange, som afvigelser forekommer vedrørende planlagt og faktisk startdato samt planlagt og faktisk slutdato for arbejdsordren.</span><span class="sxs-lookup"><span data-stu-id="88a26-154">The **Occurrences** fields show the number of times deviations occur in relation to scheduled and actual start date, and scheduled and actual end date on the work order.</span></span>

